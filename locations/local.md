# Local

An embedded service in Jolie can communicate with its embedder exploiting the `local` medium. `local` communications uses the shared memory between embedded and embedder services in order to handle message delivery in an lightweight and efficient way.

The `local` medium needs no protocol when used into a port definition and it could be followed by an internal local label which univocally identifies the service within the embedded group.

An example using this medium can be found in part "Handling structured messages and embedder's operations invocation" of [Embedding Java Services](https://jolielang.gitbook.io/docs/architectural-composition/embedding_java) subsection.

The `local` medium can be used for service internal self communications, as shown in the example below:

```text
include "runtime.iol"
include "string_utils.iol"

type HanoiRequest: void{
    .src: string
    .aux: string
    .dst: string
    .n: int
    .sid?: string
}

type HanoiReponse: void {
    .move?: string
}

interface LocalOperations{
    RequestResponse:
        hanoiSolver( HanoiRequest )( HanoiReponse )
}

interface ExternalOperations{
    RequestResponse:
        hanoi( HanoiRequest )( string )
}

outputPort Self{
    Interfaces: LocalOperations
}

inputPort Self {
    Location: "local"
    Interfaces: LocalOperations
}

inputPort PowerService {
    Location: "socket://localhost:8000"
    Protocol: http{
        .format = "html"
    }
    Interfaces: ExternalOperations
}

execution { concurrent }

init
{
    getLocalLocation@Runtime()( Self.location )
}

main
{
    [ hanoi( request )( response ){
        getRandomUUID@StringUtils()(request.sid);
        hanoiSolver@Self( request )( subRes );
        response = subRes.move
    }]{ nullProcess }

    [ hanoiSolver( request )( response ){
        if ( request.n > 0 ){
            subReq.n = request.n;
            subReq.n--;
            with( request ){
                subReq.aux = .dst;
                subReq.dst = .aux;
                subReq.src = .src;
                subReq.sid = .sid
            };
            hanoiSolver@Self( subReq )( response );
            response.move +=     "
" + 
                                ++global.counters.(request.sid) + 
                                ") Move from " + request.src +
                                " to " + request.dst + ";";
            with ( request ){
                subReq.src = .aux;
                subReq.aux = .src;
                subReq.dst = .dst
            };
            hanoiSolver@Self( subReq )( subRes );
            response.move += subRes.move
        }
    }]{ nullProcess }
}
```

The operation `hanoi` receives an external http request \(e.g., a GET `http://localhost:8000/hanoi?src=source&aux=auxiliary&dst=destination&n=5`\) and fires the local operation `hanoiSolver` which uses the `local` location for recursively call itself and build the solution.


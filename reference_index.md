# Reference Index

This reference index is still under construction. If you spot something missing, please consider [contributing](https://github.com/jolie/docs/blob/master/reference_index.md)!

## Basic Data Types

* `bool`: booleans;
* `int`: integers;
* `long`: long integers \(with `L` or `l` suffix\);
* `double`: double-precision float \(decimal literals\);
* `string`: strings;
* `raw`: byte arrays;
* `void`: the empty type.

[Go to section: Handling Simple Data](https://github.com/jolie/docs/tree/b09339d5f67a4343dbdab600b5ea7903dd9f1e1d/basics/handling_simple_data/README.md)

## Tree operators

* `<<`: deep copy. [Go to section: Copying an entire tree structure](basics/data_structures.md#less-than-less-than-copying-an-entire-tree-structure)
* `->`: alias. [Go to section: Structure aliases](basics/data_structures.md#greater-than-structures-aliases)

## Behavioural operators

* `;`: sequence. [Go to section: Sequence](basics/composing_statements.md#sequence)
* `|`: parallel. [Go to section: Parallel](basics/composing_statements.md#parallel)

## Statements

* `^`: "freezing" operator. [Go to section: Termination and Compeonsation](https://jolielang.gitbook.io/docs/basicsfault-handling/termination_and_compensation#installation-time-variable-evaluation)
* `[..]{..}`: input choice. [Go to section: Input Choice](basics/composing_statements.md#input-choice)
* `Aggregates`: aggregation statement. [Go to section: Aggregation](architectural-composition/aggregation.md)
* `cH`: handler placeholder. [Go to section: Termination and Compeonsation](https://jolielang.gitbook.io/docs/basics/fault-handling/termination_and_compensation)
* `comp()`: compensation statement. [Go to section: Termination and Compeonsation](https://jolielang.gitbook.io/docs/basics/fault-handling/termination_and_compensation)
* `constants`: constants definition. [Go to section: Constants](basics/constants.md)
* `courier`: courier process definition. [Go to section: Couriers](architectural-composition/couriers.md)
* `cset`: cset definition. [Go to section: Sessions](basics/sessions.md)
* `csets`: csets assignment. [Go to section: Sessions](basics/sessions.md)
* `default`: fautl name alias. [Go to section: Scopes and Faults](basics/fault-handling/basics.md#accessing-a-fault-caught-in-a-scope-the-alias-default)
* `define`: procedure definition. [Go to section: Define](basics/define.md)
* `embedded`: embedding statement. [Go to section: Embedding](architectural-composition/embedding.md)
* `execution { single | concurrent | sequential }`: execution modality. [Go to section: Processes](basics/processes.md)
* `for(){}`: deterministic loop. [Go to section: for and while](basics/composing_statements.md#for-and-while)
* `foreach(:){}`: traversing items. [Go to section: foreach](basics/data_structures.md#foreach-traversing-items)
* `forward`: forward statement. [Go to section: Couriers](architectural-composition/couriers.md#the-statement-forward)
* `global`: global variables. [Go to section: Processes](basics/processes.md)
* `if (..) {..} else {..}`: conditional statement. [Go to section: Conditions and conditional statement](basics/composing_statements.md#conditions-and-conditional-statement)
* `init{}`: init scope. [Go to section: Processes and Sessions](basics/processes.md)
* `inputPort`: input port statement. [Go to section: Ports](basics/communication-ports/ports.md)
* `interface`: interface definition. [Go to section: Interfaces](basics/interfaces/)
* `interface extender`: interface extension. [Go to section: Couriers](architectural-composition/couriers#interface-extension)
* `Interfaces`: port interfaces. [Go to section: Interfaces](basics/interfaces/)
* `install()`: handler installation. [Go to section: Scopes and Faults](basics/fault-handling/basics.md)
* `Location`: port location. [Go to section: Locations](https://github.com/jolie/docs/tree/b09339d5f67a4343dbdab600b5ea7903dd9f1e1d/basics/communication-ports/locations.md)
* `main{}`: main scope. [Go to section: Processes](basics/processes.md)
* `new`: generation of a fresh token. [Go to section: Sessions](basics/sessions.md)
* `OneWay`: one way operation definition. [Go to section: Interfaces](https://github.com/jolie/docs/tree/b09339d5f67a4343dbdab600b5ea7903dd9f1e1d/basics/communication-ports/interfaces/README.md)
* `outputPort`: output port statement. [Go to section: Ports](https://github.com/jolie/docs/tree/b09339d5f67a4343dbdab600b5ea7903dd9f1e1d/basics/communication-ports/ports/README.md)
* `Protocol`: port protocol. [Go to section: Protocol](https://github.com/jolie/docs/tree/b09339d5f67a4343dbdab600b5ea7903dd9f1e1d/basics/communication-ports/protocol/README.md)
* `provide [] until []`: provide until statement. [Go to section: Sessions](basics/sessions.md#the-provide-until-statement)
* `Redirects`: redirection statement. [Go to section: Redirection](architectural-composition/redirection.md)
* `RequestResponse`: request response operation definition. [Go to section: Interfaces](basics/interfaces/)
* `service`: internal service definition. [Go to section: Internal Services](architectural-composition/internal_services.md)
* `scope(){}`: scope definition. [Go to section: Scopes and Faults](basics/fault-handling/basics.md)
* `synchronized(){}`: variables synchronization. [Go to section: Processes](basics/processes.md)
* `spawn( .. over .. )  in .. {}`: spawn primitive definition. [Go to section: Dynamic Parallel](basics/dynamicparallel.md)
* `this`: termination handler reference. [Go to section: Termination and Compeonsation](https://jolielang.gitbook.io/docs/basics/fault-handling/termination_and_compensation)
* `throw(){}`: fault raising. [Go to section: Scopes and Faults](basics/fault-handling/basics.md)
* `throws`: fault raising declaration. [Go to section: Interfaces](basics/interfaces/)
* `type`: type definition. [Go to section: Data Types](https://github.com/jolie/docs/tree/b09339d5f67a4343dbdab600b5ea7903dd9f1e1d/basics/communication-ports/data_types/README.md)
* `undef()`: undefines a variable. [Go to section: Undef](basics/data_structures.md#undef-erasing-tree-structures)
* `while(){}`: conditional loop. [Go to section: for and while](basics/composing_statements.md#for-and-while)
* `with`: interface extender operator. [Go to section: Couriers](architectural-composition/couriers#interface-extension)
* `with(:){}`: shortcut to repetitive variable paths. [Go to section: with](basics/data_structures.md#with-a-shortcut-to-repetitive-variable-paths)

## Tools and related projects

* `jolie2surface`: surface generation tool. [Go to section: jolie2surface](architectural-composition/aggregation.md#jolie-2-surface)


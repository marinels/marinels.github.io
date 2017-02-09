##  Composing Streams

* Observables can be composed using operators <!-- .element: class="fragment" -->
* Operators adjust the resulting observable <!-- .element: class="fragment" -->
    * creation, transform, filter, combine, math, backpressure, reduce, side effect
* Operators are declarative, similar to LINQ <!-- .element: class="fragment" -->

----

### Some Pseudocode

Each line (other than source) is an operator being applied in the _pipeline_

```plain
source
    filter elements on text starts with "a"
    buffer elements every 10 seconds into an array
    transform elements into array length
    exclude duplicate consecutive values
```

note:

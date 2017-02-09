##  Next, Error, and Complete

* <!-- .element: class="fragment" --> `next` provides event handling
* <!-- .element: class="fragment" --> `error` provides error handling
* <!-- .element: class="fragment" --> `complete` provides stream completion handling
* <!-- .element: class="fragment" --> `subscribe` can be called with no arguments

----

### Events

* Act as a termination to the stream composition <!-- .element: class="fragment" -->
* Fired for every event <!-- .element: class="fragment" -->

----

### Errors

* Must be provided if any error handling is required <!-- .element: class="fragment" -->
* If omitted, errors will bubble up synchronously and kill the stream asynchronously <!-- .element: class="fragment" -->
* Will fire once after an error then the stream will die <!-- .element: class="fragment" -->

----

### Completion

* Optional <!-- .element: class="fragment" -->
* Called at most once <!-- .element: class="fragment" -->
* Not called if stream has an error <!-- .element: class="fragment" -->

note:

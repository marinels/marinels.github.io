##  Side Effects

* Global mutable state is (<!-- .element: class="fragment" -->_generally_) bad
* Side effects are observable stream actions that modify global state <!-- .element: class="fragment" -->
* Side effect actions can be applied to events, errors, and completion <!-- .element: class="fragment" -->

----

### Reasons to Use Side Effects

* Broadcast patterns (i.e., <!-- .element: class="fragment" -->_logging_) are great uses of side effects
* Circular dependencies (<!-- .element: class="fragment" -->_avoid if possible_) may require side effects
* Great for debugging certain stream operators <!-- .element: class="fragment" -->

```ts
source
    .filter(x => x === 1)
    .do(x => { debugger; })
    .subscribe();
```

<!-- .element: class="fragment" -->

note:

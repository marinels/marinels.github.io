##  Subjects

* Subjects are a special part of Rx <!-- .element: class="fragment" -->
* They act as both an <!-- .element: class="fragment" --> **Observable** and an **Observer**
* They can consume an observable and produce events <!-- .element: class="fragment" -->
* They also support interactive events <!-- .element: class="fragment" -->

---

### BehaviourSubject

* <!-- .element: class="fragment" --> **BehaviourSubject** persists the most recent value
* You can introspect the current value of this subject <!-- .element: class="fragment" -->

---

### ReplaySubject

* <!-- .element: class="fragment" --> **ReplaySubject** emits its most recent value to new observers
* You can additionally emit <!-- .element: class="fragment" --> *n* most recent values

note:

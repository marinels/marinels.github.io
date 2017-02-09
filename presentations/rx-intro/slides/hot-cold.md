##  Hot &amp; Cold

* Observables come in two flavors <!-- .element: class="fragment" -->
* Hot observables fire events whether an observer is watching or not <!-- .element: class="fragment" -->
* Cold observables only fire events once an observer is watching <!-- .element: class="fragment" -->

---

### Hot Observables

* E.g., Click events. You can't defer them! <!-- .element: class="fragment" -->
* No observers means events evaporate <!-- .element: class="fragment" -->
* Convert cold to hot by using a <!-- .element: class="fragment" --> `Subject`

---

### Cold Observables

* E.g., <!-- .element: class="fragment" --> `Observable.from([1, 2, 3])`. Nothing happens until you watch
* Every observer observes the same stream <!-- .element: class="fragment" -->
* Convert hot to cold by using <!-- .element: class="fragment" --> `publish` or `share` operators

note:

##  A Short Example

* [**Tetris**! A completely reactive implemetation](http://bokuweb.github.io/rxjs-tetris/)
* View the [Source code](https://github.com/bokuweb/rxjs-tetris)

---

### How it works

* All in the <!-- .element: class="fragment" --> [index.ts](https://github.com/bokuweb/rxjs-tetris/blob/master/src/index.ts) file
* keyboard events are observed <!-- .element: class="fragment" -->
* Shapes move down every <!-- .element: class="fragment" --> `500ms`
* <!-- .element: class="fragment" --> `actionSource$` used for demultiplexing events
* game state iterates on <!-- .element: class="fragment" --> `actionSource$` events
* game state events trigger <!-- .element: class="fragment" --> `render` calls via `subscribe`

note:
    none

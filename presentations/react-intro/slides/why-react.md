##  Why React?

* Components are **Modular** and **Encapsulated**
* Views are Composed **Declaratively**
* Rendering is **Fast** and **Efficient**

---

## Modularity & Encapsulation

* We can break down complex web components into **discrete** units of functionality and rendering
* Each simple component must only worry about its **own** inputs and Rendering
* Larger *composite* components simply **manage** flow of control to sub-components 

---

## Declarative Composition

* JSX (and *TSX*) allows inline composition of component structure
* Extensible `JSX.Element` class allows easy creation of custom components
* Many libraries that have *Reactified* popular web components

---

## Fast & Efficient Rendering

* The **Virtual DOM** intercepts DOM modifications to compute DOM *diffs*
* Updated DOM nodes replace existing DOM nodes to minimize re-rendering time
* Each component controls its own re-rendering conditions

note:
    none

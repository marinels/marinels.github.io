##  Why React?

* Components are **Modular** and **Encapsulated**
* Views are Composed **Declaratively**
* Rendering is **Fast** and **Efficient**
* Compatible with **TypeScript**

---

## Modularity & Encapsulation

* We can break down complex web components into **discrete** units of functionality and rendering
    * This improves coding **efficiency** and **maintainability**
* Each simple component must only worry about its **own** inputs and Rendering
    * We can much more easily write **testable** components that perform **one** job **really well**
    * Components adjust their logic and rendering based **entirely** on inputs
* Larger *composite* components simply **manage** flow of control to sub-components
    * **Minimal** logic in these componets, only communication for **coordination**
    * Rely primary on the work of the sub-components

---

## Declarative Composition

* JSX (and *TSX*) allows inline composition of component structure
    * **HTML** tags embedded within your **JavaScript** or **TypeScript** code
    * No need to write UI and UI bindings in **seperate files**
    * No need to represent UI component structure with code
* Extensible `lang-ts namespace JSX` and `lang-ts class React.Component`
    * `lang-ts namespace JSX` can extend `lang-ts interface IntrinsicElements` to create new **HTML** tags
    * `lang-ts class React.Component` extensions create new `React` component **HTML** tags
* Many libraries that have *Reactified* popular web components
    * `react-bootstrap` is a popular *reactified* library (more on this later)

---

## Fast & Efficient Rendering

* The **Virtual DOM** intercepts DOM modifications to compute DOM *diffs*
    * Your **JSX**/**TSX** produces a **metadata** structure used to perform DOM **comparisons**
* Updated DOM nodes replace existing DOM nodes to minimize re-rendering time
    * A **significant** difference from *Angular*, which re-renders the **entire** DOM
* Each component controls its own re-rendering conditions
    * **Optimize** rendering by breaking up high frequency changes into sub-components

note:
    none

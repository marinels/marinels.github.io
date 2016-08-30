##  react-bootstrap

* This is a **React** framework to augment Twitter's **bootstrap** to be easy to use with **React**
* All components have been converted into **React** components with appropriate inputs
* Any missing parts can still be accessed using plain old **CSS* classes

---

#### The Grid System

```html
<Grid>
    <Row>
        <Col sm={6}>Left Half</Col>
        <Col sm={6}>Right Half</Col>
    </Row>
</Grid>
```

* Use `lang-html <Grid>`, `lang-html <Row>`, `lang-html <Col>`, and `lang-html <Clearfix />` components
* `lang-html <Grid>` will style the gutter with a margin automatically
    * use the `fill` property expand the grid horizontally
* `lang-html <Row>` eliminate the `lang-html <Grid>` margin (useful for **flush** layouts)
* `lang-html <Col>` allows defining columns and responsive breaks
    * Break on various screen sizes: `xs`, `sm`, `md`, `lg`
    * Push, Pull, and Offset for any screen size
* `lang-html <Clearfix />` will consume the vertical space within a parent block
    * Useful for **vertically aligning** blocks that contain only float elements

---

#### Less Styling

* Bootstrap uses `Less` to style components
    * You can make use of existing `Less` variables defined by **bootstrap**
* Import the bootstrap `Less` definitions to use any defined variables or mixins
* Create your own styles in `Less` or `CSS`
    * Import these files using standard imports
    * `lang-ts import './MyComponent.less`

---

#### Component Usage

* Simply `lang-ts import` the components you need from `react-bootstrap` in your `*.tsx` file
    * `lang-ts import { Button, Label, Badge } from 'react-bootstrap'`
    * Use intellisense for component props
* Compose complex or domain specific components using containment

note:
    none

##  A Short Example

* We will build a basic **Button** component that will allow us to customize the button text *per instance*
* We will be able to optionally prepend a label as well as define a custom `click` function

---

#### Import the React library

```ts
import * as React from 'react';
```

* The React library is exported **globally** as a single entry point
* We must then import the entry point (`*`) into an alias (`React`)
* We can then make use of `React` exports by accessing properties on the `React` alias
* Always import `React` when using **TSX**, even if you don't use the `React` alias

---

#### Define the Input Properties

```ts
export interface LabelButtonProps {
  text: string;
  label?: any;
  onClick?: Function;
}
```

* Component input properties are defined as an **interface** (*contract*) for that component
* Note that both `label` and `onClick` are suffixed with a `?`
    * This indicates that both are optional input parameters
    * `text` on the other hand is a **required** parameter
* Note that `label` is typed as `lang-ts any`
    * This indicates that we can pass in any value (including another **component**!)

---

#### Declare the Component Class

```ts
export class LabelButton extends React.Component<LabelButtonProps, any> {
  // ...
}
```

* Using **TypeScript**, we can assign typings for the **input** props and component **state**
* extend `lang-ts React.Component<P, S>` to create a composable **Component**
    * `P` is the input properties interface type
    * `S` is the component state interface type
* We are using `lang-ts any` for the state typing because our component has no state
    * This means our component is not expected to dynamically re-render itself

---

#### Setup Default Parameter Values

```ts
  static defaultProps = {
    label: 'My Button',
  };
```

* We need only define a static object with `key`/`value` pairs to setup input defaults
* If no property is provided at *composition*, then `lang-ts 'My Button'` is used as a default

---

#### Define our Encapsulated Click Handler

```ts
  private onClick() {
    if (this.props.onClick != null) {
      this.props.onClick.apply(null, arguments);
    }
  }
```

* By defining the function locally, we can ensure that our button's composition is sound
    * our button clicks will always at least hit this *internal* function
* If a click handler was provided at composition (as an input), then we **forward** the call onwards

---

#### Define our Rendering Logic

```
  render() {
    return (
      <div className='LabelButton'>
        { this.props.label == null ? null : <div className='LabelButton-label'>{ this.props.label }</div> }
        <button className='LabelButton-button' onClick={ this.onClick }>{ this.props.text }</button>
      </div>
    );
  }
```

* We can render **JSX**/**TSX** directly within a function
    * We need to inform typescript's `tsconfig.json` that `lang-json "jsx": "react"`
    * We can only render this markup in a `*.jsx` or `*.tsx`
* We can define expression blocks using **curly-braces**
    * These are expressions only, statements are not permitted
    * Prepare more complex variables before the return statement and reference them here
* We use `lang-ts className` instead of `lang-ts class` on **HTML** tags
    * The value is rendered as `lang-ts class`
    * We can use `npm` module `classnames` to perform **dynamic** *classing* of tags

---

#### Component Containment

```
  render() {
    return (
      <div className='ContainerButton'>
        <button className='ContainerButton-button' onClick={ this.onClick }>{ this.props.children }</button>
      </div>
    );
  }

// ...

<ContainerButton onClick={ () => { console.log('clicked!'); } }>
  <span>This is the button content</span>
</ContainerButton>
```

* React supports containment using a special `lang-ts props.children`
* This allows us to supply complex internal structure to the component
    * The component doesn't need to know about how to render it's children

note:
    none

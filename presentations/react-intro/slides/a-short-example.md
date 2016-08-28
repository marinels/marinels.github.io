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

---

#### Define the Input Properties

```ts
export interface LabelButtonProps {
  text: string;
  label?: any;
  onClick?: Function;
}
```

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

* extend `lang-ts React.Component<P, S>` to create a composable **Component**
    * `P` is the input properties interface type
    * `S` is the component state interface type
* Using **TypeScript**, we can assign typings for the **input** props and component **state**
* We are using `lang-ts any` for the state generic typing because our component has no state

---

#### Setup Default Parameter Values

```ts
  static defaultProps = {
    label: 'My Button',
  };
```

* If no property is provided at *composition*, then *My Button* is used as a default

---

#### Define our Encapsulated Click Handler

```ts
  private onClick() {
    if (this.props.onClick != null) {
      this.props.onClick.apply(null, arguments);
    }
  }
```

* By defining the function locally, we can ensure that our button's compositiono is sound
* If a click handler was provided at composition, then we forward the call onwards

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
    * We need to inform typescript's `tsconfig.json` that `"jsx": "react"`
    * We can only render this markup in a `*.jsx` or `*.tsx`
* We can define expression blocks using **curly-braces**
    * These are expressions only, statements are not permitted
* We use `className` instead of `lang-ts class`
    * the value is passed on and rendered as `lang-ts class`

note:
    
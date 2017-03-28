# react-outside-click-handler

React Component for handling some specific component outside click

**Table of contents**

- [Installation](#installation)
- [API](#api)
  - `<OutsideClickHandler onOutsideClick useCapture />`
- [Example](#example)
- [Development](#development)
- [Credits](#credits)

# Installation

```bash
yarn add react-outside-click-handler
```

# API

- `<OutsideClickHandler onOutsideClick useCapture />`

### props

- `onOutsideClick` (*Function*): outside click handler
- `useCapture` (*Boolean*): See [link's useCapture section](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

# Example

```jsx
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.handleOutsideClick = this.handleOutsideClick.bind(this);
  }

  handleOutsideClick() {
    // ...
  }

  render() {
    return (
      <div>
        <TodoList>
          <Todo />
          ...
        </TodoList>
        <OutsideClickHandler onOutsideClick={this.handleOutsideClick}>
          <InsideComponent />
        </OutsideClickHandler>
      </div>
    );
  }
}
```

# Development

```bash
yarn start
```

Then, Go to `http://localhost:3000`

# Credits

This component is inspired by [airbnb/react-dates's OutsideClickHandler](https://github.com/airbnb/react-dates/blob/master/src/components/OutsideClickHandler.jsx)

# Licence

MIT @ [Taehwan, No (taehwanno)](https://github.com/taehwanno)

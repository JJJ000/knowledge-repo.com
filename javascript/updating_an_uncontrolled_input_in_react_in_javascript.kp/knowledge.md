---
title: Altering an uncontrolled input using react
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `onChange` event to update the value of an uncontrolled input in React.
---

**Contents**

[TOC]

#### Using Refs

React provides a way to access the underlying DOM nodes of a component using `refs`. 

We can use the `ref` attribute on an input element, and assign it to a class property. This property will then be populated with the DOM node when the component mounts.

Once we have access to the DOM node, we can call `.value` on it to set the value of the input.

```js
class MyInput extends React.Component {
  constructor(props) {
    super(props);
    this.inputRef = React.createRef();
  }

  componentDidMount() {
    this.inputRef.current.value = 'My new value';
  }

  render() {
    return <input ref={this.inputRef} />;
  }
}
```

#### Using State

We can also use the `state` of the component to keep track of the value of the input.

We can use the `onChange` event handler to update the `state` when the value of the input changes.

Then, we can use the `value` attribute on the input to set the initial value of the input to the value stored in the `state`.

```js
class MyInput extends React.Component {
  constructor(props) {
    super(props);
    this.state = { value: 'My new value' };
  }

  handleChange = (event) => {
    this.setState({ value: event.target.value });
  };

  render() {
    return (
      <input
        value={this.state.value}
        onChange={this.handleChange}
      />
    );
  }
}
```

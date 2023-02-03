---
title: What is the best way to give an input field focus after it has been rendered?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Call the input`s focus() method after rendering.
---

**Contents**

[TOC]

# Solution 1: Using Refs

1. Create a ref in the component class:

```js
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.inputRef = React.createRef();
  }
  ...
}
```

2. Pass the ref to the input element:

```js
<input type="text" ref={this.inputRef} />
```

3. Set the focus in componentDidMount lifecycle method:

```js
componentDidMount() {
  this.inputRef.current.focus();
}
```

# Solution 2: Using Focus

1. Set the autoFocus prop on the input element:

```js
<input type="text" autoFocus />
```

2. Create a method to set focus on the input element:

```js
setFocus() {
  this.input.focus();
}
```

3. Call the method in componentDidMount lifecycle method:

```js
componentDidMount() {
  this.setFocus();
}
```

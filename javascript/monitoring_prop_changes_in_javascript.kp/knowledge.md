---
title: What steps should I take to monitor changes to 'props'?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the componentDidUpdate() lifecycle method to listen for changes in props.
---

**Contents**

[TOC]

1. Using the `componentWillReceiveProps()` Lifecycle Method

This lifecycle method allows you to detect changes in props and respond accordingly. It is invoked whenever a component receives new props and is passed the new props as its only argument.

```js
componentWillReceiveProps(nextProps) {
  if (this.props.someProp !== nextProps.someProp) {
    // do something
  }
}
```

2. Using the `shouldComponentUpdate()` Lifecycle Method

This lifecycle method allows you to detect changes in props and decide whether or not the component should re-render. It is invoked before a component is re-rendered and is passed the new props and state as its only arguments.

```js
shouldComponentUpdate(nextProps, nextState) {
  if (this.props.someProp !== nextProps.someProp) {
    return true; // component will update
  } else {
    return false; // component will not update
  }
}
```

3. Using the `getDerivedStateFromProps()` Lifecycle Method

This lifecycle method allows you to detect changes in props and update the state accordingly. It is invoked when a component is receiving new props and is passed the new props and the current state as its only arguments.

```js
static getDerivedStateFromProps(nextProps, prevState) {
  if (nextProps.someProp !== prevState.someProp) {
    return {
      someProp: nextProps.someProp
    };
  }
  return null;
}
```

4. Using the `componentDidUpdate()` Lifecycle Method

This lifecycle method allows you to detect changes in props and perform side effects accordingly. It is invoked immediately after a component is updated and is passed the previous props and state as its only arguments.

```js
componentDidUpdate(prevProps, prevState) {
  if (this.props.someProp !== prevProps.someProp) {
    // do something
  }
}
```

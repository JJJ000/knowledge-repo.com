---
title: Send properties to the parent component in react.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: A React component can pass props to its parent component using the built-in function `this.props.onUpdate()`.
---

**Contents**

[TOC]

#### Passing Props

Props are passed from a parent component to a child component in React.js using the `props` object. The `props` object is an object that contains all the properties that were passed to the child component from the parent component.

#### Using Props

Props can be accessed in the child component using the `this.props` keyword. For example, if a parent component passes a prop called `name`, it can be accessed in the child component by writing `this.props.name`.

#### Updating Props

Props are immutable, meaning they cannot be changed. However, a parent component can update the props it passes to a child component by calling the `setState()` method. This method will cause the component to re-render and the updated props will be passed to the child component.

#### Passing Callback Functions

In addition to passing props, parent components can also pass callback functions to child components. These functions can be used to update the state of the parent component in response to events that occur in the child component. This is done by passing a function as a prop, and then calling that function in the child component when the event occurs.

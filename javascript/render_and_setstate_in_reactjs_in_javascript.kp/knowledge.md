---
title: Does 'render' get invoked whenever 'setstate' is invoked in reactjs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, render is only called when the component state or props have changed.
---

**Contents**

[TOC]

### No

Render is not called any time setState is called in JavaScript. This is because render is a React-specific method, and setState is a JavaScript method.

### React Component Lifecycle

When setState is called, the React component lifecycle is triggered. This includes a series of methods such as componentWillReceiveProps, shouldComponentUpdate, and componentDidUpdate. The render method is not called directly by setState, but it is called indirectly as part of the lifecycle.

### setState

The setState method is used to update the state of a React component. It is called with an object containing the new state values that need to be updated. This object is merged with the existing state, and the new values are applied to the component.

### render

The render method is used to render the component to the DOM. It is called whenever the component needs to be re-rendered, such as when the state changes or when a prop is updated. The render method is not called directly by setState, but it is called indirectly as part of the component lifecycle.

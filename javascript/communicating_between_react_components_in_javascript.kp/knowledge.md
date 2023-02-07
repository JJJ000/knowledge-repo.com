---
title: What is the best way to share information between related react components?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use props or state to pass data between related React components.
---

**Contents**

[TOC]

1. **Using Props**

Props are a simple way to pass data from one component to another. When a parent component passes data to a child component, it is called a prop. Props are read-only and cannot be modified by the child component.

2. **Using Context**

Context provides a way to pass data through the component tree without having to pass props down manually at every level. Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.

3. **Using State**

State is similar to props, but it is private and fully controlled by the component. State is a JavaScript object that stores a component’s dynamic data and determines the component’s behavior. A component can access its own state and update it, but it cannot access or modify the state of its parent or child components.

4. **Using Refs**

Refs provide a way to access the underlying DOM element or a React component instance. Refs should be avoided in most cases, but they can be useful when you need direct access to a DOM element or an instance of a component.

---
title: What is the best way to change the state of a parent component in react?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Call the parent component`s setState() method with the updated state.
---

**Contents**

[TOC]

#1 React setState

The most common way to update the parent's state in React is to use the `setState` method. This method allows you to update the state of a component and re-render it with the new state. To use `setState`, you need to pass in an object containing the new state.

#2 Passing a Callback Function

Another way to update the parent's state in React is to pass a callback function as a prop to the child component. The child component can then call the callback function, which will update the parent's state.

#3 Using Context

If your application is using React's Context API, you can update the parent's state by using the `setState` method in the context provider. This allows you to update the state of the parent component from the child component.

#4 Using Redux

Finally, if you are using a Redux store in your application, you can update the parent's state by dispatching an action. This allows you to update the state of the parent component from anywhere in your application.

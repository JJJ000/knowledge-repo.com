---
title: React cannot accept objects as a child component
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: React elements should be either a string or a number, or React components.
---

**Contents**

[TOC]

# What is an 'Object' in Javascript?
An object in Javascript is a collection of key-value pairs that can store data, represent a real-world entity or a function. Objects are enclosed in curly braces {} and can contain primitive data types, arrays, other objects, and functions.

# What is a 'React Child'?
A React child is a single element or a component that is rendered by a React component. It can be a string, a number, a React element, or an array of any of these elements.

# Why are Objects Not Valid React Children?
Objects are not valid React children because they cannot be rendered directly. React requires a single element or component to be passed as a child, and objects cannot be represented as a single element.

# What Can Be Used Instead of Objects?
Instead of using objects, React components can be used to represent data or functions. React components can be used to render data or logic in a way that can be represented as a single element or component. This allows React to render the data or logic in the way that it is intended.

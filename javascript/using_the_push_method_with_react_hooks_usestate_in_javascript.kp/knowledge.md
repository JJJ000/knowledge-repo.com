---
title: What is the usestate() hook's push method in react?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The useState hook`s setter function can be used to push an item to an array, similar to the Array.prototype.push() method.
---

**Contents**

[TOC]

1. Introduction
2. What is the useState Hook?
3. How to use the useState Hook's push Method
4. Conclusion

## Introduction

React Hooks are a new feature in React that allow developers to use state and other React features without writing a class. The useState Hook is a built-in Hook that allows developers to add local state to a function component. The useState Hook's push method allows developers to add new items to an array in React state.

## What is the useState Hook?

The useState Hook is a built-in Hook that allows developers to add local state to a function component. It takes a single argument, which is the initial state, and returns an array with two elements. The first element is the current state, and the second element is a function that allows the state to be updated.

## How to use the useState Hook's push Method

To use the useState Hook's push method, you must first declare a state variable with the useState Hook. Then, you can use the push method to add a new item to the array. The push method takes the item to be added as an argument.

For example, let's say you have an array of numbers in your state:

```javascript
const [numbers, setNumbers] = useState([1, 2, 3]);
```

To add a new number to the array, you can use the push method:

```javascript
setNumbers([...numbers, 4]);
```

The spread operator (...) is used to create a new array with all the elements from the original array, plus the new element.

## Conclusion

The useState Hook's push method allows developers to add new items to an array in React state. It takes the item to be added as an argument, and the spread operator (...) can be used to create a new array with all the elements from the original array, plus the new element.

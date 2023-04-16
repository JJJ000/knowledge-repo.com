---
title: Warnings for using async functions in react hooks' useeffect the useeffect function must either return a cleanup function or nothing
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, if an async function is used in useEffect, it must return either a cleanup function or nothing.
---

**Contents**

[TOC]

**Section 1: What is a React Hook Warning?**

A React Hook warning is an alert that is triggered when a user attempts to use a hook incorrectly. Hooks are a new feature in React that allow developers to use state and other React features without writing a class component. When a hook is used incorrectly, React will output a warning to the console. 

**Section 2: What is an Async Function?**

An async function is a function that is declared with the keyword “async”. Async functions are designed to allow a function to execute asynchronous code, meaning that the code can be executed without blocking the main thread. Async functions can be used to perform tasks such as making API calls, fetching data, and doing other background tasks. 

**Section 3: What is UseEffect?**

UseEffect is a React hook that is used to perform side effects in a React component. It is called after every render, and it allows the user to perform tasks such as making API calls, setting up subscriptions, and updating the DOM.

**Section 4: What is the React Hook Warning for an Async Function in UseEffect?**

The React Hook Warning for an async function in useEffect is that the useEffect function must return a cleanup function or nothing. This means that if an async function is used in the useEffect, the function must return a cleanup function that will be called when the effect is unmounted, or it must return nothing. If the function does not return a cleanup function or nothing, React will output a warning to the console.

---
title: Utilize the async/await feature when mapping through an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can use async await with Array.map in Javascript to execute asynchronous operations within the map loop.
---

**Contents**

[TOC]

### 1. What is Array.map?
Array.map is a method in Javascript that is used to create a new array from an existing array by manipulating each element in the existing array. It takes a callback function as an argument, which is used to manipulate each element in the array.

### 2. What is Async Await?
Async Await is a way of writing asynchronous code in Javascript. It allows us to write code that is more readable and easier to maintain. It uses the keywords `async` and `await` to make asynchronous code look more like synchronous code.

### 3. How to Use Array.map with Async Await?
We can use Array.map with Async Await by wrapping the callback function in an async function. This allows us to use the `await` keyword to wait for each element in the array to be processed before continuing.

### 4. Example
Here is an example of how to use Array.map with Async Await:

```js
const array = [1, 2, 3];

const result = await Promise.all(
  array.map(async element => {
    const data = await fetchData(element);
    return data;
  })
);
```
In this example, the `fetchData` function is called for each element in the array and the results are stored in the `result` variable.

---
title: Advantages and disadvantages of using redux-saga with es6 generators compared to redux-thunk with es2017 async/await
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Redux-saga with ES6 generators offers more control over async logic, while redux-thunk with ES2017 async/await provides a more concise syntax.
---

**Contents**

[TOC]

**Pros of Using Redux-Saga with ES6 Generators**

1. Readability: Generators allow for more readable code, as they are able to separate out different tasks and make the code easier to follow.

2. Easy to Test: Generators are easy to test, as the code can be broken up into smaller chunks and tested in isolation.

3. Error Handling: Generators make it easy to handle errors, as the code can be written in a way that allows for more granular control over error handling.

**Cons of Using Redux-Saga with ES6 Generators**

1. Complexity: Generators can be complex to use, as they require an understanding of the ES6 generator syntax.

2. Performance: Generators can be slower to execute than other solutions, as they require the code to be paused and resumed at certain points.

**Pros of Using Redux-Thunk with ES2017 Async/Await**

1. Readability: Async/Await makes the code more readable, as it allows for the code to be written in a more natural way.

2. Performance: Async/Await is faster to execute than other solutions, as it allows for the code to be executed in parallel.

3. Flexibility: Async/Await is flexible, as it allows for the code to be written in a way that can be adapted to different scenarios.

**Cons of Using Redux-Thunk with ES2017 Async/Await**

1. Complexity: Async/Await can be complex to use, as it requires an understanding of the ES2017 async/await syntax.

2. Error Handling: Async/Await can be difficult to handle errors, as the code can be written in a way that makes it difficult to control how errors are handled.

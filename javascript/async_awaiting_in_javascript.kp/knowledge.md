---
title: Await can only be used inside of an asynchronous function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, await can only be used inside an async function.
---

**Contents**

[TOC]

**Yes:**

- Async functions
- Syntax

Async functions are functions that allow the use of the `await` keyword. The `await` keyword can only be used inside an async function and it is used to pause the execution of the function until a Promise is resolved. The syntax of an async function is as follows:

```javascript
async function myFunction() {
    // code here
    let result = await somePromise();
    // code here
}
```

**No:**

- Generators
- Syntax

Generators are functions that allow the use of the `yield` keyword. The `yield` keyword can be used inside a generator function and it is used to pause the execution of the function until a Promise is resolved. The syntax of a generator function is as follows:

```javascript
function* myGenerator() {
    // code here
    let result = yield somePromise();
    // code here
}
```

In this case, the `await` keyword cannot be used as it is not valid syntax in generator functions.

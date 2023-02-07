---
title: Provide arguments to the setinterval function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The setInterval() function takes two parameters a function to be executed and the time interval (in milliseconds) between executions.
---

**Contents**

[TOC]

1. Syntax: 

`setInterval(function, milliseconds, param1, param2, ...)`

2. Parameters: 

- **function**: The function that will be executed.
- **milliseconds**: The number of milliseconds (thousandths of a second) that the interval should wait before executing the code.
- **param1, param2, ...**: Optional additional parameters that can be passed to the function.

3. Examples: 

```
// Pass two parameters to the function
setInterval(myFunc, 1000, "Hello", "World");

// Pass three parameters to the function
setInterval(myFunc, 1000, "Foo", "Bar", "Baz");
```

4. Notes:

- The parameters are optional and can be omitted if not needed.
- The parameters are passed to the function in the same order as they are specified in the setInterval call.

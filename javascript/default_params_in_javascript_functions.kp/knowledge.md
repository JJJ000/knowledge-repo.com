---
title: Specify a default argument for a JavaScript function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A default parameter value for a JavaScript function can be set by assigning a value to the parameter in the function declaration.
---

**Contents**

[TOC]

### Syntax

```
function funcName(param1 = defaultValue) { 
    // function body 
}
```

### Example

```
function greeting(name = "John") { 
    console.log("Hello " + name); 
}
```

### Explanation

In the above example, the parameter `name` is given a default value of `John` if it is not provided when the function is called.  If the function is called without any argument, it will use the default value.

---
title: Cancel the setinterval function in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: ClearInterval() can be used to stop a setInterval() call.
---

**Contents**

[TOC]

# 1. Set Interval

The `setInterval()` method calls a function or evaluates an expression at specified intervals (in milliseconds).

# 2. Stopping Interval

The `clearInterval()` method stops the interval that was set with the `setInterval()` method.

# 3. Syntax

The syntax for the `clearInterval()` method is:

```javascript
clearInterval(intervalID);
```

# 4. Example

```javascript
var intervalID = setInterval(myFunc, 1000);

// stop interval after 10 seconds
setTimeout(function(){
    clearInterval(intervalID);
}, 10000);
```

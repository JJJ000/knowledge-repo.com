---
title: Run the setinterval function immediately without delay
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The setInterval function can be executed without delay by passing 0 as the second argument.
---

**Contents**

[TOC]

## Section 1 - Setting an Interval

The setInterval() method in JavaScript is used to set a timer which executes a given function repeatedly at every given time-interval. This method takes two parameters: a callback function and a time-interval in milliseconds.

## Section 2 - Executing Without Delay

The setInterval() method can be executed without delay the first time by passing 0 as the second argument. This will cause the callback function to be executed immediately without any delay.

## Section 3 - Example

```
// setInterval without delay
setInterval(function(){
    console.log("Hello World");
}, 0);
```

## Section 4 - Output

The above code will output "Hello World" immediately without any delay.

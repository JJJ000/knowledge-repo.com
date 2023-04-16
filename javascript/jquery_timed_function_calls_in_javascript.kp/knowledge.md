---
title: How can I use jquery to call a function every 5 seconds?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the setInterval() method with a callback function and an interval of 5000 milliseconds.
---

**Contents**

[TOC]

### Set Interval

The easiest way to call a function every 5 seconds in jQuery is to use the `setInterval` method. This method takes two arguments: a function and a time interval in milliseconds. The function will be called repeatedly, starting after the time interval has elapsed.

```javascript
setInterval(function(){
  // code to be executed
}, 5000);
```

### Clear Interval

It is important to note that `setInterval` returns a unique ID which can be used to clear the interval. If the interval is not cleared, it will continue to execute the function every 5 seconds. This can be done using the `clearInterval` method, which takes the unique ID returned by `setInterval` as an argument.

```javascript
var intervalID = setInterval(function(){
  // code to be executed
}, 5000);

clearInterval(intervalID);
```

### jQuery

Finally, if jQuery is being used, the `setInterval` and `clearInterval` methods can be wrapped in jQuery functions to make them easier to use. For example, the `setInterval` method can be wrapped in a `jQuery.fn.interval` function, and the `clearInterval` method can be wrapped in a `jQuery.fn.clearInterval` function.

```javascript
jQuery.fn.interval = function(func, time){
  return setInterval(func, time);
};

jQuery.fn.clearInterval = function(id){
  clearInterval(id);
};
```

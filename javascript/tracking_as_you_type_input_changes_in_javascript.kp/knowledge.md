---
title: What is the most effective way to monitor changes made to an input field of type "text" while typing?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The best way to track onchange as-you-type in input type=`text` in Javascript is to use the oninput event.
---

**Contents**

[TOC]

1. Using the `oninput` Event: 
The `oninput` event is triggered when the value of an element changes, either as a result of user interaction or programmatically. It is supported by all major browsers, including Internet Explorer 9 and later. To track the `oninput` event for an `input` element, you can use the following code:

```
document.getElementById("inputId").oninput = function(){
   // code to execute when the input changes
};
```

2. Using the `onkeyup` Event: 
The `onkeyup` event is triggered when a key is released while the element is in focus. It is supported by all major browsers, including Internet Explorer 9 and later. To track the `onkeyup` event for an `input` element, you can use the following code:

```
document.getElementById("inputId").onkeyup = function(){
   // code to execute when a key is released
};
```

3. Using the `onchange` Event: 
The `onchange` event is triggered when an element loses focus and its value has been modified since gaining focus. It is supported by all major browsers, including Internet Explorer 9 and later. To track the `onchange` event for an `input` element, you can use the following code:

```
document.getElementById("inputId").onchange = function(){
   // code to execute when the input loses focus and its value has been modified
};
```

4. Using the `setInterval` Function: 
The `setInterval` function can be used to check the value of an `input` element at regular intervals. This method is not as reliable as the other methods mentioned above, as it is dependent on the interval set. To track the `input` element with the `setInterval` function, you can use the following code:

```
var input = document.getElementById("inputId");
setInterval(function(){
   // code to execute when the input changes
}, 1000); // check every 1000 milliseconds
```

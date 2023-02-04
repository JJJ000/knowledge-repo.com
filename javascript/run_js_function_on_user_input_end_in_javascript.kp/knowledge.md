---
title: Trigger a JavaScript function when the user has finished typing instead of on each key press
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the `onchange` event to run a Javascript function when the user finishes typing.
---

**Contents**

[TOC]

## Using setTimeout

Using the `setTimeout` function, you can wait for a certain amount of time before running the desired JavaScript function. This is useful for when you want to wait until the user has finished typing before running the function.

```javascript
// Set a timer for 1 second
let timer = setTimeout(myFunction, 1000);

// Function to run after timer has finished
function myFunction() {
  // Do something
}

// If the user starts typing again, clear the timer
document.addEventListener('keyup', () => {
  clearTimeout(timer);
});
```

## Using debounce

Another way to achieve this is by using a debounce function. A debounce function is a function that will only run after a certain amount of time has passed since the last time it was called. This is useful for when you want to wait until the user has finished typing before running the function.

```javascript
// Create a debounce function
function debounce(func, wait) {
  let timeout;
  return function executedFunction() {
    const context = this;
    const args = arguments;
    
    const later = function() {
      timeout = null;
      func.apply(context, args);
    };

    clearTimeout(timeout);
    timeout = setTimeout(later, wait);
  };
};

// Add an event listener to the document
document.addEventListener('keyup', debounce(myFunction, 1000));

// Function to run after debounce timer has finished
function myFunction() {
  // Do something
}
```

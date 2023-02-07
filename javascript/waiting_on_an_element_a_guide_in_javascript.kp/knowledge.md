---
title: What is the best way to wait for an element to appear?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use an interval loop to check if the element exists, and break out of the loop when the element is found.
---

**Contents**

[TOC]

# Section 1: Using a Polling Function

A polling function is a function that continually checks if an element exists. The code below creates a polling function that checks for the existence of an element with the ID of "myElement" every 100 milliseconds. Once the element is found, the function will return true and the loop will end.

```
function elementExists() {
  let myElement = document.getElementById("myElement");
  if (myElement) {
    return true;
  }
  setTimeout(elementExists, 100);
}
```

# Section 2: Using MutationObserver

MutationObserver is an API that allows you to watch for changes in the DOM. The code below creates a MutationObserver that watches for the addition of an element with the ID of "myElement". Once the element is added, the observer will call the callback function and the loop will end.

```
let observer = new MutationObserver(function(mutations) {
  mutations.forEach(function(mutation) {
    let myElement = mutation.addedNodes[0];
    if (myElement.id === "myElement") {
      callback(myElement);
      observer.disconnect();
    }
  });
});

observer.observe(document.body, { childList: true });
```

# Section 3: Using requestIdleCallback

requestIdleCallback is an API that allows you to schedule a callback function to be called when the browser is idle. The code below creates a requestIdleCallback that will check for the existence of an element with the ID of "myElement". Once the element is found, the callback function will be called and the loop will end.

```
let idleCallback = requestIdleCallback(function(deadline) {
  let myElement = document.getElementById("myElement");
  if (myElement) {
    callback(myElement);
    cancelIdleCallback(idleCallback);
  }
});
```

# Section 4: Using Promise

Promise is an API that allows you to create a function that will resolve when a condition is met. The code below creates a promise that will resolve when an element with the ID of "myElement" is found. Once the element is found, the promise will resolve and the loop will end.

```
let promise = new Promise(function(resolve, reject) {
  let myElement = document.getElementById("myElement");
  if (myElement) {
    resolve(myElement);
  } else {
    setTimeout(promise, 100);
  }
});
```

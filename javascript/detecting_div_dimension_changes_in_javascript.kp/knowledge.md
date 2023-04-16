---
title: What are the methods for determining if the size of a div has changed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The dimensions of a DIV can be detected by listening for the `resize` event on the element.
---

**Contents**

[TOC]

## Using the `resize` Event

The `resize` event is fired when the size of an element has changed. It can be used to detect when the size of a `div` element has changed.

To use the `resize` event, add an `addEventListener` to the `div` element and listen for the `resize` event.

```js
myDiv.addEventListener('resize', function () {
  // Do something when the size of the div changes
});
```

## Using the `offsetHeight` Property

The `offsetHeight` property of a `div` element is the height of the element including padding and borders, but not margin. By comparing the `offsetHeight` of a `div` element before and after it has been resized, it is possible to detect when the size of a `div` element has changed.

```js
let myDivHeight = myDiv.offsetHeight;

// Do something to resize the div

if (myDiv.offsetHeight !== myDivHeight) {
  // The size of the div has changed
}
```

## Using the `getBoundingClientRect` Method

The `getBoundingClientRect` method of a `div` element returns an object containing the size of the element. By comparing the size of the element before and after it has been resized, it is possible to detect when the size of a `div` element has changed.

```js
let myDivRect = myDiv.getBoundingClientRect();

// Do something to resize the div

if (myDiv.getBoundingClientRect().width !== myDivRect.width ||
    myDiv.getBoundingClientRect().height !== myDivRect.height) {
  // The size of the div has changed
}
```

## Using the `MutationObserver`

The `MutationObserver` is a JavaScript API that can be used to detect changes to the DOM. It can be used to detect when the size of a `div` element has changed.

To use the `MutationObserver`, create a `MutationObserver` and pass it a callback function that will be called when the size of the `div` element has changed.

```js
let observer = new MutationObserver(function (mutations) {
  mutations.forEach(function (mutation) {
    if (mutation.type === 'attributes' &&
        mutation.attributeName === 'style') {
      // The size of the div has changed
    }
  });
});

observer.observe(myDiv, {
  attributes: true
});
```

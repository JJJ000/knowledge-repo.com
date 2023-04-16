---
title: What is the best way to detect a click outside a specific element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use an event listener on the document object to detect a click outside an element.
---

**Contents**

[TOC]

## Using Event Listeners

The easiest way to detect a click outside an element is to add an event listener to the document object for the `click` event. 

When a click event is triggered, we can then use the `event.target` property to determine which element was clicked. If the clicked element does not match the element we are interested in, then we know that the click was outside the element.

## Example

```javascript
document.addEventListener('click', function(event) {
    // If the clicked element doesn't have the right selector, bail
    if (!event.target.matches('.outside-click-element')) return;

    // Do something...
});
```

## Using jQuery

If you are using jQuery, you can use the `.on()` method to attach an event handler to the document object.

```javascript
$(document).on('click', function(event) {
    // If the clicked element doesn't have the right selector, bail
    if (!$(event.target).is('.outside-click-element')) return;

    // Do something...
});
```

## Using CSS

It is also possible to detect a click outside an element using CSS. This can be done using the `:not()` selector, which allows you to select all elements that do not match a given selector.

```css
*:not(.outside-click-element):active {
    /* Do something... */
}
```

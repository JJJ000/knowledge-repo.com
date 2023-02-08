---
title: What are the coordinates of a mouse click on a canvas element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `onclick` event to get the x and y coordinates of the mouse click on the canvas element.
---

**Contents**

[TOC]

## Getting the Coordinates

The `getBoundingClientRect()` method can be used to get the position of the canvas relative to the viewport, and the `clientX` and `clientY` properties of the `MouseEvent` object can be used to get the position of the mouse relative to the viewport. To get the mouse coordinates relative to the canvas, these values can be subtracted from each other.

## Adding an Event Listener

An event listener must be added to the canvas in order to detect when the mouse is clicked. This can be done with the `addEventListener()` method, which takes two arguments: the type of event to listen for (in this case, `click`) and a callback function to execute when the event occurs.

## Callback Function

The callback function should take a `MouseEvent` object as an argument. This object can then be used to get the mouse coordinates relative to the canvas, as described in the previous section.

## Output

The coordinates of the mouse click can then be outputted in whatever format is desired. For example, they could be logged to the console or used to draw a shape on the canvas.

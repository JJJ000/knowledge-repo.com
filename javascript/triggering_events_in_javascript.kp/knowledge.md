---
title: What is the process for initiating an event in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Triggering an event in JavaScript can be done by using the EventTarget.dispatchEvent() method.
---

**Contents**

[TOC]

## Method 1: Using the `on` Method
The `on` method is used to assign an event handler to an element. This method takes two arguments: the event type and the event handler.

```javascript
document.getElementById('myButton').on('click', myFunction);
```

The `myFunction` is the event handler that will be triggered when the element is clicked.

## Method 2: Using the `addEventListener` Method
The `addEventListener` method is used to assign an event handler to an element. This method takes three arguments: the event type, the event handler, and a boolean value indicating whether the event should be triggered only once or multiple times.

```javascript
document.getElementById('myButton').addEventListener('click', myFunction, false);
```

The `myFunction` is the event handler that will be triggered when the element is clicked.

## Method 3: Using the `dispatchEvent` Method
The `dispatchEvent` method is used to manually trigger an event. This method takes one argument: the event object.

```javascript
var clickEvent = new Event('click');
document.getElementById('myButton').dispatchEvent(clickEvent);
```

The `clickEvent` is the event object that will be dispatched when the element is clicked.

## Method 4: Using the `trigger` Method
The `trigger` method is a jQuery method used to manually trigger an event. This method takes one argument: the event type.

```javascript
$('#myButton').trigger('click');
```

The `click` is the event type that will be triggered when the element is clicked.

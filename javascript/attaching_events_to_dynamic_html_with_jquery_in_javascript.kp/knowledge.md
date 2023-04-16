---
title: What is the best way to add event listeners to dynamically created html elements using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use jQuery`s `on` method to attach events to dynamic HTML elements.
---

**Contents**

[TOC]

1. Select the Element
2. Attach the Event

**1. Select the Element**

To attach an event to a dynamic HTML element, the first step is to select the element. This can be done using the jQuery selector syntax. For example, to select all `<a>` tags, you could use the following code: 

```javascript
$('a')
```

If the element has an ID or class, you can also use the `#` or `.` syntax to select it. For example, to select an element with an ID of `myElement`, you could use the following code:

```javascript
$('#myElement')
```

**2. Attach the Event**

Once the element is selected, you can attach the event using the `.on()` method. This method takes two parameters: the event type and a callback function. For example, to attach a click event to the selected element, you could use the following code:

```javascript
$('#myElement').on('click', function() {
    // Do something
});
```

The callback function will be called whenever the event is triggered. In this example, it will be called when the element is clicked.

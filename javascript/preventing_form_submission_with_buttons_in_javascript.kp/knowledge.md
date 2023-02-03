---
title: What is the best way to stop buttons from submitting forms?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Prevent buttons from submitting forms in Javascript by using the `onclick` event to call a function that returns false.
---

**Contents**

[TOC]

### 1. Stop Propagation

Using the `stopPropagation()` method on the event object, we can prevent the form from submitting when a button is clicked. This method stops the event from bubbling up the DOM tree, preventing any parent handlers from being notified of the event.

### 2. Return False

We can also return `false` from the event handler, which will prevent the form from submitting. This is useful when we don't want to execute any other code in the event handler.

### 3. PreventDefault

The `preventDefault()` method on the event object can be used to prevent the default action of the event from being triggered. In the case of a form submission, this will prevent the form from submitting.

### 4. Use Type="Button"

We can also use the `type="button"` attribute on the button element to prevent it from submitting the form. This is the recommended way to prevent form submission, as it is more explicit than the other methods.

---
title: Event.preventdefault() prevents the default action of an event from being triggered, while return false stops the further execution of the function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: event.preventDefault() prevents the default action of an element from happening, while return false does the same but also stops the event from bubbling up the DOM tree.
---

**Contents**

[TOC]

### preventDefault

The `preventDefault()` method is used to prevent the default action of an element from occurring. For example, it can be used to prevent a submit button from submitting a form. This method can be used on most event types, such as mouse, keyboard, and form events.

### return false

The `return false` statement is used to halt the execution of a function or event handler. It is commonly used in event handlers to prevent the default action of an element from occurring. For example, it can be used to prevent a submit button from submitting a form. It is also used to prevent a link from redirecting the user to another page.

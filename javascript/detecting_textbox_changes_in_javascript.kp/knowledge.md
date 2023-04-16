---
title: What are the indicators of a textbox's content being modified?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `onchange` event handler to detect when a textbox`s content has changed.
---

**Contents**

[TOC]

1. Using the `onchange` Event
--------------------------------
The `onchange` event is triggered when the value of an element has been changed. The `onchange` event is mainly used on `<input>` elements, such as text fields and textareas, as well as `<select>` elements.

The syntax for using the `onchange` event is:
```html
<element onchange="myScript">
```

2. Using the `oninput` Event
-----------------------------
The `oninput` event is triggered when the value of an element is changed. It is similar to the `onchange` event, but the `oninput` event occurs immediately after the value of an element has changed, while the `onchange` event occurs when the element loses focus.

The syntax for using the `oninput` event is:
```html
<element oninput="myScript">
```

3. Using the `keyup` Event
--------------------------
The `keyup` event is triggered when a key is released on the keyboard. This event is often used to detect when a user has finished typing in a text field or textarea.

The syntax for using the `keyup` event is:
```html
<element onkeyup="myScript">
```

4. Using the `onpropertychange` Event
-------------------------------------
The `onpropertychange` event is triggered when the value of an element is changed. It is supported by Internet Explorer and is often used to detect when a user has finished typing in a text field or textarea.

The syntax for using the `onpropertychange` event is:
```html
<element onpropertychange="myScript">
```

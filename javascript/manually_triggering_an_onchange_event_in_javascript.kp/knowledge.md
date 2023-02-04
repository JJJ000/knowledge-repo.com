---
title: What is the method for initiating an onchange event manually?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Trigger an onchange event manually in Javascript by calling the element`s `dispatchEvent` method.
---

**Contents**

[TOC]

### Method 1: Using .dispatchEvent()

The `.dispatchEvent()` method can be used to trigger an onchange event manually. The `.dispatchEvent()` method takes an event object as an argument.

```javascript
// Create a new event object
let event = new Event('change');

// Trigger the onchange event
document.getElementById('myInput').dispatchEvent(event);
```

### Method 2: Using .trigger()

The `.trigger()` method is a jQuery method that can be used to trigger an onchange event manually.

```javascript
// Trigger the onchange event
$('#myInput').trigger('change');
```

### Method 3: Using .click()

The `.click()` method can also be used to trigger an onchange event manually. This method is most commonly used when the desired element is a checkbox or radio button.

```javascript
// Trigger the onchange event
document.getElementById('myInput').click();
```

---
title: Enter a value into the input field
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: document.getElementById(`inputID`).value = `newValue`;
---

**Contents**

[TOC]

### Get Input Element

To set the value of an input field in Javascript, the first step is to get the input element. This can be done using the `document.querySelector()` or `document.getElementById()` methods. For example:

```javascript
const inputElement = document.querySelector('#myInput');
```

### Set Value

Once the input element is obtained, the `value` property can be used to set the value of the input field. For example:

```javascript
inputElement.value = 'My new value';
```

### Trigger Event

Finally, to ensure that any event handlers attached to the input element are triggered, the `input` event can be manually triggered. For example:

```javascript
inputElement.dispatchEvent(new Event('input'));
```

### Example

Putting it all together, the following code can be used to set the value of an input field in Javascript:

```javascript
const inputElement = document.querySelector('#myInput');
inputElement.value = 'My new value';
inputElement.dispatchEvent(new Event('input'));
```

---
title: Find all elements with a "data-xxx" attribute without using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: document.querySelectorAll(`[data-xxx]`);
---

**Contents**

[TOC]

**Section 1: Get Elements with data-xxx Attribute**

We can use the `document.querySelectorAll` method to select all elements with a `data-xxx` attribute.

```javascript
const elements = document.querySelectorAll('[data-xxx]');
```

**Section 2: Iterate Over Elements**

Once we have the elements, we can iterate over them using a `for` loop.

```javascript
for (let i = 0; i < elements.length; i++) {
  const element = elements[i];
  // Do something with element
}
```

**Section 3: Access Data Attribute Value**

Within the loop, we can access the data attribute value using the `getAttribute` method.

```javascript
const dataValue = element.getAttribute('data-xxx');
```

**Section 4: Use Data Attribute Value**

Finally, we can use the data attribute value in our code.

```javascript
if (dataValue === 'foo') {
  // Do something
}
```

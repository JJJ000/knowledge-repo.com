---
title: Delete element by id
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: document.getElementById(`id`).remove();
---

**Contents**

[TOC]

### Using getElementById

The `getElementById` method is used to access an element in the DOM (Document Object Model) using its ID. This method returns a single element, so it is best used when you know the exact ID of the element you want to access.

```javascript
const element = document.getElementById('element-id');
element.parentNode.removeChild(element);
```

### Using querySelector

The `querySelector` method is used to access an element in the DOM using a CSS selector. This method returns the first element that matches the selector, so it is best used when you have a specific selector for the element you want to access.

```javascript
const element = document.querySelector('#element-id');
element.parentNode.removeChild(element);
```

### Using removeChild

The `removeChild` method is used to remove an element from the DOM. This method requires a reference to the element to be removed, so it is best used when you already have a reference to the element you want to remove.

```javascript
const element = document.getElementById('element-id');
element.parentNode.removeChild(element);
```

### Using remove

The `remove` method is used to remove an element from the DOM. This method does not require a reference to the element to be removed, so it is best used when you don't have a reference to the element you want to remove.

```javascript
document.getElementById('element-id').remove();
```

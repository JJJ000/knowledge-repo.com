---
title: What is the process for deactivating all elements within a div?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `.disabled` property to set the `disabled` attribute on all div elements.
---

**Contents**

[TOC]

### Using the `style` Property

You can disable all content within a `div` element using the `style` property.

```javascript
document.getElementById('div-id').style.display = 'none';
```

This will set the `display` property of the `div` element to `none`, which will effectively disable all content within it.

### Using the `disabled` Property

You can also disable all content within a `div` element using the `disabled` property.

```javascript
document.getElementById('div-id').disabled = true;
```

This will set the `disabled` property of the `div` element to `true`, which will effectively disable all content within it.

### Using the `visibility` Property

You can also disable all content within a `div` element using the `visibility` property.

```javascript
document.getElementById('div-id').style.visibility = 'hidden';
```

This will set the `visibility` property of the `div` element to `hidden`, which will effectively disable all content within it.

### Using the `opacity` Property

You can also disable all content within a `div` element using the `opacity` property.

```javascript
document.getElementById('div-id').style.opacity = '0';
```

This will set the `opacity` property of the `div` element to `0`, which will effectively disable all content within it.

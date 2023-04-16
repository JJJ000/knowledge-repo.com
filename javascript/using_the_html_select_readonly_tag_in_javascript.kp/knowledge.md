---
title: Select tag/input in html form with readonly attribute
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The value of a readonly SELECT tag/input in Javascript can be retrieved using the `document.getElementById()` method.
---

**Contents**

[TOC]

### Setting the Attribute

The `readonly` attribute can be set on a `<select>` element in JavaScript using the `setAttribute()` method.

```javascript
document.getElementById("mySelect").setAttribute("readonly", "readonly");
```

### Removing the Attribute

The `readonly` attribute can be removed from a `<select>` element in JavaScript using the `removeAttribute()` method.

```javascript
document.getElementById("mySelect").removeAttribute("readonly");
```

### Checking the Attribute

The `readonly` attribute can be checked on a `<select>` element in JavaScript using the `hasAttribute()` method.

```javascript
if (document.getElementById("mySelect").hasAttribute("readonly")) {
  // Element has readonly attribute
}
```

### Disabling the Element

The `<select>` element can also be disabled in JavaScript using the `disabled` attribute.

```javascript
document.getElementById("mySelect").disabled = true;
```

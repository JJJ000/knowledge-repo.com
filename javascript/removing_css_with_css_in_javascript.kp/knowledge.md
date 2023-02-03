---
title: What is the process for removing a style that was added using the .css() function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can remove a style added with .css() function in Javascript by using the .removeAttr() function.
---

**Contents**

[TOC]

### 1. jQuery

If you are using jQuery, you can use the `.removeAttr()` method to remove the style that was added with the `.css()` function.

```js
$('#myElement').removeAttr('style');
```

### 2. Vanilla JavaScript

If you are not using jQuery, you can use the `.removeProperty()` method to remove the style that was added with the `.css()` function.

```js
document.getElementById('myElement').style.removeProperty('style');
```

### 3. Remove All Styles

If you want to remove all styles that were added with the `.css()` function, you can use the `.removeAttribute()` method.

```js
document.getElementById('myElement').removeAttribute('style');
```

### 4. Reset to Default

If you want to reset the style to its default value, you can use the `.css()` method with an empty string as the value.

```js
$('#myElement').css('style', '');
```

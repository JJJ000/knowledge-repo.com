---
title: What is the process for determining if an element is hidden using jquery?
authors:
- smooth_flow
tags:
- javascript
- jquery
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can check if an element is hidden in jQuery by using the .is(`hidden`) method.
---

**Contents**

[TOC]

### Using the jQuery `.is()` Method

The jQuery `.is()` method can be used to check whether an element is hidden or not. This method returns a boolean value, `true` if the element is hidden, and `false` if it is visible.

Syntax:
```javascript
$(selector).is(':hidden')
```

Example:
```javascript
$('#myElement').is(':hidden');
```

### Using the jQuery `.css()` Method

The jQuery `.css()` method can also be used to check if an element is hidden. This method returns a string value that can be used to check if the element is hidden or not.

Syntax:
```javascript
$(selector).css('display')
```

Example:
```javascript
$('#myElement').css('display') === 'none';
```

### Using the jQuery `.is()` Method with `:visible`

The jQuery `.is()` method can also be used with the `:visible` argument to check if an element is visible or not. This method returns a boolean value, `true` if the element is visible, and `false` if it is hidden.

Syntax:
```javascript
$(selector).is(':visible')
```

Example:
```javascript
$('#myElement').is(':visible');
```

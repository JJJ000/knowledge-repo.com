---
title: Toggle a checkbox's checked/unchecked state using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the `checked` property to check or uncheck a checkbox with JavaScript.
---

**Contents**

[TOC]

**Using Checkbox Object:**

1. Get the Checkbox Object: 

```javascript
// Get the checkbox
let checkbox = document.getElementById("checkbox");
```

2. Set the Checkbox State: 

```javascript
// Check the checkbox
checkbox.checked = true;

// Uncheck the checkbox
checkbox.checked = false;
```

**Using Input Element:**

1. Get the Input Element: 

```javascript
// Get the input element
let input = document.getElementById("input");
```

2. Set the Input State: 

```javascript
// Check the input
input.checked = true;

// Uncheck the input
input.checked = false;
```

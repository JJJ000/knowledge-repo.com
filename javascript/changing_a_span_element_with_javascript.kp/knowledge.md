---
title: What is the syntax for altering the text of a span element using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the innerHTML property to set the text of a span element using JavaScript.
---

**Contents**

[TOC]

### Selecting the Element

The first step is to select the element using the `document.querySelector()` method. This will return the first element that matches the specified selector.

```javascript
const element = document.querySelector('span');
```

### Changing the Text

Once the element has been selected, the text can be changed by setting the `innerText` property of the element.

```javascript
element.innerText = 'New Text';
```

### Using a Variable

If the text is stored in a variable, the variable can be used to set the `innerText` property.

```javascript
const newText = 'New Text';
element.innerText = newText;
```

### Using a Function

If a function is used to set the text, the function can be called when setting the `innerText` property.

```javascript
const getText = () => 'New Text';
element.innerText = getText();
```

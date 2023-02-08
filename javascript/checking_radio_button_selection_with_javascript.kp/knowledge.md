---
title: What is the syntax to determine if a radio button is selected using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `checked` property on the radio button element to check if it is selected.
---

**Contents**

[TOC]

## Using `checked` Property

The `checked` property of a radio button can be used to check whether the radio button is selected or not. This property returns true if the radio button is selected and false otherwise.

```javascript
if(document.getElementById("radioButtonId").checked) {
    // Radio button is selected
}
else {
    // Radio button is not selected
}
```

## Using `querySelector`

The `querySelector` method can be used to check if a particular radio button is selected or not.

```javascript
if(document.querySelector("input[name='radioName']:checked")) {
    // Radio button is selected
}
else {
    // Radio button is not selected
}
```

## Using `querySelectorAll`

The `querySelectorAll` method can also be used to check if a particular radio button is selected or not.

```javascript
var radios = document.querySelectorAll('input[name="radioName"]');

for (var i = 0, length = radios.length; i < length; i++) {
    if (radios[i].checked) {
        // Radio button is selected
        break;
    }
}
```

## Using `for` Loop

The `for` loop can be used to check if a particular radio button is selected or not.

```javascript
var radios = document.getElementsByName('radioName');

for (var i = 0, length = radios.length; i < length; i++) {
    if (radios[i].checked) {
        // Radio button is selected
        break;
    }
}
```

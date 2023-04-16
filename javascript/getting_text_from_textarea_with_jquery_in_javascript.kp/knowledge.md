---
title: Retrieve the contents of a textarea using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery`s .val() method can be used to get the text from a textarea in JavaScript.
---

**Contents**

[TOC]

## Using jQuery

Using jQuery, you can get the text from a textarea using the `val()` method:

```javascript
let textareaText = $('textarea').val();
```

## Using Vanilla JavaScript

Using Vanilla JavaScript, you can get the text from a textarea using the `value` property of the `textarea` element:

```javascript
let textareaText = document.querySelector('textarea').value;
```

## Using the DOM

You can also get the text from a textarea using the DOM `innerText` property of the `textarea` element:

```javascript
let textareaText = document.querySelector('textarea').innerText;
```

## Using the HTML DOM

Lastly, you can get the text from a textarea using the `innerHTML` property of the `textarea` element:

```javascript
let textareaText = document.querySelector('textarea').innerHTML;
```

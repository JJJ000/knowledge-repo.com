---
title: Retrieve the class names of an element using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: $(selector).get(0).classList can be used to get the class list for an element with jQuery in Javascript.
---

**Contents**

[TOC]

## Section 1: Get the Element

Using jQuery, you can get the element you are looking for by using the `$()` function. For example, if you wanted to get an element with the ID of `example`, you would do this:

```js
var element = $('#example');
```

## Section 2: Get the Class List

Once you have the element, you can use the `.attr()` method to get the class list. This will return a string with the classes separated by spaces.

```js
var classes = element.attr('class');
```

## Section 3: Split the Class List

Now that you have the class list as a string, you can use the `.split()` method to split the string into an array of classes.

```js
var classList = classes.split(' ');
```

## Section 4: Use the Class List

Now that you have the class list as an array, you can use it however you need. For example, you could loop through the array and do something with each class.

```js
classList.forEach(function(cls) {
  // Do something with each class
});
```

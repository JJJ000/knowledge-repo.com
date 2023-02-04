---
title: Iterate through elements with the same class using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use a jQuery `.each()` loop to iterate over a collection of elements with the same class.
---

**Contents**

[TOC]

**Section 1: Selecting Elements**

To select elements with the same class in jQuery, you can use the `$('.className')` selector. This will return a jQuery object containing all elements with the specified class name.

**Section 2: Looping Through Elements**

Once the elements have been selected, you can loop through them using the `.each()` method. This method will take a function as an argument and will execute the function on each element in the jQuery object.

**Section 3: Function Syntax**

The function that is passed to the `.each()` method should have the following syntax: 

```js
$('.className').each(function() {
    // Do something with the current element
});
```

**Section 4: Example**

For example, if you wanted to add a class to each element with the class `.example-class`, you could use the following code:

```js
$('.example-class').each(function() {
    $(this).addClass('new-class');
});
```

---
title: Removing items from an array in JavaScript - using the 'delete' keyword versus the 'splice' method
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Delete removes an element from an array, while splice can remove and add elements from an array.
---

**Contents**

[TOC]

## delete

The `delete` operator is used to remove a property from an object. It takes the object and the name of the property as its arguments and will delete the property from the object. The `delete` operator will return `true` if the property was successfully deleted and `false` if it was not.

## splice

The `splice` method is used to remove elements from an array. It takes the array and the index of the element to be removed as its arguments and will remove the element from the array. The `splice` method will return an array containing the removed elements. 

## Advantages of delete

The `delete` operator is useful when you want to remove a single property from an object. It is also faster than the `splice` method.

## Advantages of splice

The `splice` method is useful when you want to remove multiple elements from an array. It is also more flexible than the `delete` operator, as it can be used to add elements to an array as well as remove them.

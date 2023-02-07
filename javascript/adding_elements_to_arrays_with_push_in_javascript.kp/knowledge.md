---
title: Does array.push() exist?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, there is no built-in method to push an item to an array if it does not exist.
---

**Contents**

[TOC]

#### What is push()?

The `push()` method adds one or more elements to the end of an array and returns the new length of the array.

#### Does push() add elements to an array if they don't exist?

No, the `push()` method does not add elements to an array if they don't exist. It only adds elements to the end of an array if they already exist.

#### How can we add elements to an array if they don't exist?

We can use the `includes()` method to check if an element exists in an array. If the element does not exist, we can use the `push()` method to add the element to the end of the array.

#### Example

```javascript
let myArray = [1, 2, 3];

let element = 4;

if (!myArray.includes(element)) {
  myArray.push(element);
}

console.log(myArray); // [1, 2, 3, 4]
```

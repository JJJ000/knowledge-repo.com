---
title: What is the best way to add something to an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the push() method to append an element to an array in Javascript.
---

**Contents**

[TOC]

# Section 1: Declare the Array

In order to append something to an array in Javascript, the first step is to declare the array. This can be done using the following syntax:

```javascript
var arrayName = [item1, item2, item3];
```

# Section 2: Push Items to the Array

Once the array is declared, items can be pushed to the array using the `push()` method. This is done by passing the item to be added to the end of the array as an argument. For example:

```javascript
arrayName.push(item4);
```

# Section 3: Check the Array Contents

Finally, it is always a good idea to check the contents of the array to make sure the item was added correctly. This can be done by using the `console.log()` method and passing the array name as the argument. For example:

```javascript
console.log(arrayName);
```

# Section 4: Output

The output of the above code should be something like this:

```javascript
[item1, item2, item3, item4]
```

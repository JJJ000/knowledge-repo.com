---
title: Transfer an array item from one index to another
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Array.prototype.move = function (old\_index, new\_index) {this.splice(new\_index, 0, this.splice(old\_index, 1)[0]);};
---

**Contents**

[TOC]

### Step 1: Access the Element

In order to move an array element from one array position to another, we must first access the element. We can do this by using the array index to access the element. 

```
let arr = ["a", "b", "c", "d", "e"];
let element = arr[2]; // element = "c"
```

### Step 2: Remove the Element

Once we have accessed the element, we can then remove it from the array. To do this, we can use the `splice()` method. This method takes two parameters: the index of the element to be removed, and the number of elements to remove.

```
let arr = ["a", "b", "c", "d", "e"];
let element = arr[2]; // element = "c"
arr.splice(2, 1); // arr = ["a", "b", "d", "e"]
```

### Step 3: Insert the Element

Now that we have removed the element from its original position, we can insert it into the new position. To do this, we can use the `splice()` method again. This time, we will pass three parameters: the index of the position to insert the element, the number of elements to remove (which in this case is 0 since we are not removing any elements), and the element itself.

```
let arr = ["a", "b", "d", "e"];
let element = "c";
arr.splice(2, 0, element); // arr = ["a", "b", "c", "d", "e"]
```

### Step 4: Return the Array

Finally, we can return the array with the element in its new position.

```
let arr = ["a", "b", "c", "d", "e"];
return arr; // ["a", "b", "c", "d", "e"]
```

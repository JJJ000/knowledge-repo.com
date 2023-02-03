---
title: Adding the contents of one array to the end of another array without creating a new array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.push.apply() method to extend an existing array with another array.
---

**Contents**

[TOC]

# Section 1: Using Spread Operator
The spread operator (...) can be used to extend an existing JavaScript array with another array. The syntax for using the spread operator is as follows:

`let newArray = [...existingArray, ...otherArray];`

The spread operator will take the elements from the existing array and other array and combine them into a new array. 

# Section 2: Using Concat Method
The concat() method can also be used to extend an existing array with another array. The syntax for using the concat() method is as follows:

`let newArray = existingArray.concat(otherArray);`

The concat() method will take the elements from the existing array and other array and combine them into a new array.

# Section 3: Using Push Method
The push() method can also be used to extend an existing array with another array. The syntax for using the push() method is as follows:

`let newArray = existingArray.push(...otherArray);`

The push() method will take the elements from the other array and add them to the end of the existing array.

# Section 4: Using For Loop
A for loop can also be used to extend an existing array with another array. The syntax for using a for loop is as follows:

```
for (let i = 0; i < otherArray.length; i++) {
  existingArray.push(otherArray[i]);
}
```

The for loop will iterate over the elements in the other array and add them to the end of the existing array.

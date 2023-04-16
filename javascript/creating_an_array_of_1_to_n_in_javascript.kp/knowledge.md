---
title: Creating an array containing the numbers 1 through n
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create an array using the Array.from() static method and pass in a map() callback to fill the array with numbers from 1 to N.
---

**Contents**

[TOC]

# Section 1: Create an Empty Array

Create an empty array using the `Array` constructor:

```javascript
let myArray = new Array();
```

# Section 2: Iterate Through N

Iterate through a loop to add each number from 1 to N to the array:

```javascript
for(let i = 1; i <= N; i++) {
  myArray.push(i);
}
```

# Section 3: Output the Array

Output the array to the console:

```javascript
console.log(myArray);
```

# Section 4: Final Code

The final code should look like this:

```javascript
let myArray = new Array();

for(let i = 1; i <= N; i++) {
  myArray.push(i);
}

console.log(myArray);
```

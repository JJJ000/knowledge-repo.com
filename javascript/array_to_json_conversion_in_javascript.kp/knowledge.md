---
title: Transform array into json
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The array can be converted to JSON by using the JSON.stringify() method.
---

**Contents**

[TOC]

### Using JSON.stringify

The `JSON.stringify()` method converts a JavaScript array into a JSON string.

```javascript
let array = [1, 2, 3, 4];
let json = JSON.stringify(array);

console.log(json); // [1,2,3,4]
```

### Using for loop

We can also use a for loop to iterate through each element of the array and create a JSON string.

```javascript
let array = [1, 2, 3, 4];
let json = "[";

for (let i = 0; i < array.length; i++) {
    json += array[i];
    if (i < array.length - 1) {
        json += ",";
    }
}

json += "]";

console.log(json); // [1,2,3,4]
```

### Using forEach

We can also use the `forEach()` method to iterate through each element of the array and create a JSON string.

```javascript
let array = [1, 2, 3, 4];
let json = "[";

array.forEach((element, index) => {
    json += element;
    if (index < array.length - 1) {
        json += ",";
    }
});

json += "]";

console.log(json); // [1,2,3,4]
```

### Using map

We can also use the `map()` method to iterate through each element of the array and create a JSON string.

```javascript
let array = [1, 2, 3, 4];
let json = "[";

array.map((element, index) => {
    json += element;
    if (index < array.length - 1) {
        json += ",";
    }
});

json += "]";

console.log(json); // [1,2,3,4]
```

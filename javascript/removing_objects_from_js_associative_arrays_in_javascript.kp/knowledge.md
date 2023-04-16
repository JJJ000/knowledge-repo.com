---
title: What is the best way to delete items from a JavaScript associative array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the delete operator to remove objects from a JavaScript associative array.
---

**Contents**

[TOC]

1. Using `delete` 

The `delete` operator can be used to remove an element from an associative array. This method is preferred when the key-value pair is not needed anymore.

Syntax:
```
delete array[key];
```

Example:
```
let myArray = {
  a: 'Apple',
  b: 'Banana',
  c: 'Cherry'
};

delete myArray.b;

console.log(myArray); // { a: 'Apple', c: 'Cherry' }
```

2. Using `splice()`

The `splice()` method can be used to remove an element from an associative array. This method is preferred when the key-value pair needs to be preserved.

Syntax:
```
array.splice(key, 1);
```

Example:
```
let myArray = {
  a: 'Apple',
  b: 'Banana',
  c: 'Cherry'
};

myArray.splice('b', 1);

console.log(myArray); // { a: 'Apple', c: 'Cherry' }
```

3. Using `for-in` Loop

The `for-in` loop can be used to iterate over an associative array and remove an element from it.

Syntax:
```
for (let key in array) {
  if (key === 'targetKey') {
    delete array[key];
  }
}
```

Example:
```
let myArray = {
  a: 'Apple',
  b: 'Banana',
  c: 'Cherry'
};

for (let key in myArray) {
  if (key === 'b') {
    delete myArray[key];
  }
}

console.log(myArray); // { a: 'Apple', c: 'Cherry' }
```

4. Using `filter()`

The `filter()` method can be used to filter out an element from an associative array. This method is preferred when the key-value pair needs to be preserved.

Syntax:
```
array = array.filter(item => item.key !== 'targetKey');
```

Example:
```
let myArray = {
  a: 'Apple',
  b: 'Banana',
  c: 'Cherry'
};

myArray = myArray.filter(item => item.key !== 'b');

console.log(myArray); // { a: 'Apple', c: 'Cherry' }
```

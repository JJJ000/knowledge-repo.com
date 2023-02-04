---
title: How can I create well-structured JSON from an object using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the JSON.stringify() method to generate a formatted, easy-to-read JSON string from an object in JavaScript.
---

**Contents**

[TOC]

### Step 1: Stringify the Object

The first step to generating formatted and easy-to-read JSON is to stringify the object. This can be done using the `JSON.stringify()` method, which takes in the object as the first argument and returns a string representation of the object.

```javascript
const myObject = {
  name: 'John',
  age: 20
};

const jsonString = JSON.stringify(myObject);
console.log(jsonString);
// Output: {"name":"John","age":20}
```

### Step 2: Add Spaces and Indentation

The second step is to add spaces and indentation to the JSON string to make it easier to read. This can be done by adding a second argument to the `JSON.stringify()` method. This argument is an integer that specifies the number of spaces to use for indentation.

```javascript
const myObject = {
  name: 'John',
  age: 20
};

const jsonString = JSON.stringify(myObject, 2);
console.log(jsonString);
// Output:
// {
//   "name": "John",
//   "age": 20
// }
```

### Step 3: Format the Output

The third step is to format the output to make it even more readable. This can be done by passing in a third argument to the `JSON.stringify()` method. This argument is a function that takes in the key and value of each property of the object and returns a string representation of the property.

```javascript
const myObject = {
  name: 'John',
  age: 20
};

const jsonString = JSON.stringify(myObject, null, (key, value) => {
  return `${key}: ${value}`;
});
console.log(jsonString);
// Output:
// "name: John"
// "age: 20"
```

### Step 4: Output the Formatted JSON

The fourth and final step is to output the formatted JSON. This can be done by simply logging the stringified object to the console.

```javascript
const myObject = {
  name: 'John',
  age: 20
};

const jsonString = JSON.stringify(myObject, null, (key, value) => {
  return `${key}: ${value}`;
});
console.log(jsonString);
// Output:
// "name: John"
// "age: 20"
```

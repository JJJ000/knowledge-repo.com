---
title: Combine the elements from a keys array and a values array into an object in javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The keys and values arrays can be merged into an object using the Object.assign() function.
---

**Contents**

[TOC]

### Section 1: Combining Arrays

We can use the `Object.assign()` method to combine two arrays into an object. This method takes in two parameters: the target object (where the combined array will be stored) and the source object (the array we want to combine).

```
let keys = ["name", "age"];
let values = ["John", 20];

let obj = Object.assign({}, keys, values);

console.log(obj);
// Output: {0: "name", 1: "age", 2: "John", 3: 20}
```

### Section 2: Converting to JSON

To convert the object to JSON, we can use the `JSON.stringify()` method. This method takes in one parameter, the object we want to convert, and returns a JSON string.

```
let jsonString = JSON.stringify(obj);

console.log(jsonString);
// Output: {"0":"name","1":"age","2":"John","3":20}
```

### Section 3: Formatting JSON

To make the JSON look better, we can use the `JSON.stringify()` method with the `space` parameter. This parameter takes in an integer value and adds whitespace to the JSON string.

```
let jsonString = JSON.stringify(obj, null, 2);

console.log(jsonString);
// Output:
// {
//   "0": "name",
//   "1": "age",
//   "2": "John",
//   "3": 20
// }
```

### Section 4: Final Output

The final output of the code above is a JSON string with the combined array of keys and values.

```
{"0":"name","1":"age","2":"John","3":20}
```

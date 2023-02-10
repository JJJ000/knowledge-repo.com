---
title: What is the process for generating a JavaScript array in JSON format dynamically?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Create a new array object and use the push() method to add items to it.
---

**Contents**

[TOC]

### Section 1: Creating an Array

Creating an array in JavaScript is easy. All you need to do is define a variable and assign it to an array literal.

```js
var myArray = [];
```

### Section 2: Adding Elements

Once you have the array, you can add elements to it. You can do this by using the `push()` method.

```js
myArray.push('element1');
myArray.push('element2');
```

### Section 3: Creating a JSON Object

To create a JSON object from the array, you need to use the `JSON.stringify()` method. This will convert the array into a valid JSON string.

```js
var myJSON = JSON.stringify(myArray);
```

### Section 4: Outputting the JSON Object

Finally, you can output the JSON object to the console or a file by using the `console.log()` or `fs.writeFile()` methods.

```js
console.log(myJSON);
// or
fs.writeFile('myJSON.json', myJSON, (err) => {
  if (err) throw err;
  console.log('JSON file created!');
});
```

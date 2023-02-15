---
title: Iterate through a JSON array using php
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use a foreach loop to loop through the JSON array.
---

**Contents**

[TOC]

**Section 1: Understanding JSON**

JSON (JavaScript Object Notation) is a data format that is used to store and transfer data between two different systems. It is a lightweight format that is easy to read, write, and parse. JSON is based on a subset of the JavaScript programming language and is commonly used to transfer data between web applications and servers.

**Section 2: Accessing JSON Data**

JSON data can be accessed using JavaScript or other programming languages. In JavaScript, the data can be accessed using the dot notation or bracket notation. The dot notation is used to access a specific property of an object, while the bracket notation is used to access an array element.

**Section 3: Looping Through JSON Array**

In order to loop through a JSON array, you can use the for loop. The for loop is used to iterate over each element in the array. You can access each element by using the index of the array. The for loop will execute a block of code for each element in the array.

**Section 4: Example**

Here is an example of a for loop that is used to loop through a JSON array:

```javascript
var jsonArray = [1,2,3,4,5];

for(var i = 0; i < jsonArray.length; i++){
  console.log(jsonArray[i]);
}
```

The code above will loop through the array and print out each element of the array.

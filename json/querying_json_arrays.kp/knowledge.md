---
title: What are the array elements inside a JSON type?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In JSON, array elements can be queried by using the bracket notation (e.g. jsonObject[index]).
---

**Contents**

[TOC]

1. Accessing Array Elements
--------------------------------
The most common way to access array elements in JSON is to use the `[index]` notation. This notation allows you to access a specific element in an array by its index. For example, if you wanted to access the first element in an array named `myArray`, you would use the following syntax: 

`myArray[0]`

2. Looping Through Array Elements
---------------------------------
Another way to access array elements in JSON is to loop through them. This can be done using a `for` loop, which allows you to iterate through each element in the array. For example, if you wanted to loop through an array named `myArray`, you could use the following syntax:

`for (let i = 0; i < myArray.length; i++) {
  // Do something with myArray[i]
}`

3. Accessing Nested Array Elements
----------------------------------
If the array elements are nested inside other elements, you can use the `[index]` notation to access them. For example, if you wanted to access the first element in an array nested inside another element, you could use the following syntax: 

`myElement[0][0]`

4. Using Array Methods
----------------------
Finally, you can also use array methods to access array elements in JSON. These methods allow you to access, modify, and manipulate the elements in an array. For example, if you wanted to get the first element in an array named `myArray`, you could use the following syntax: 

`myArray.shift()`

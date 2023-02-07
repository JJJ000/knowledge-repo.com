---
title: Divide the string into two parts only at the first occurrence of the given character
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the String.split() method with the limit parameter set to 1.
---

**Contents**

[TOC]

#### Split String

```javascript
let myString = "This-is-a-string";
let splitString = myString.split("-", 1);
console.log(splitString); // Output: ["This"]
```

#### Result
The code above will split the string `myString` at the first instance of the character `-` and return the result as an array. In this case, the result will be `["This"]`.

#### Limitations
This method only works for splitting a string on the first instance of a specified character. If you need to split a string on all instances of a character, you will need to use a different approach.

#### Alternatives
If you need to split a string on all instances of a character, you can use the `String.prototype.split()` method with the `limit` parameter set to `-1`. This will split the string on all instances of the specified character. 

```javascript
let myString = "This-is-a-string";
let splitString = myString.split("-", -1);
console.log(splitString); // Output: ["This", "is", "a", "string"]
```

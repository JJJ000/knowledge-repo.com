---
title: What is the best way to divide a string based on a specific character?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the split() method to split a string at a particular character.
---

**Contents**

[TOC]

1. **Define the String**

Before you can split a string, you must first define the string. This can be done by creating a variable and assigning it a value. 

```javascript
let str = "This is a string to be split";
```

2. **Define the Character**

Once you have defined the string, you must then define the character at which you want to break the string. This can be done by creating a variable and assigning it a value. 

```javascript
let char = " ";
```

3. **Split the String**

Now that you have both the string and the character defined, you can split the string by using the `split()` method. This method takes the character as an argument and returns an array containing the substrings of the original string. 

```javascript
let arr = str.split(char);
```

4. **Print the Array**

Finally, to see the result, you can print the array to the console. 

```javascript
console.log(arr);
```

This will print the following:

```
[ 'This', 'is', 'a', 'string', 'to', 'be', 'split' ]
```

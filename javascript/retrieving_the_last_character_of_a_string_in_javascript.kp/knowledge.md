---
title: What is the syntax for retrieving the final character of a string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The last character of a string can be accessed using the charAt() method, passing in the string`s length minus one as the argument.
---

**Contents**

[TOC]

#1 Using the charAt() Method

The charAt() method is a built-in JavaScript string method that allows us to get the character at a specific index within a string. To get the last character of a string, we can use the charAt() method with the string's length minus one as the index argument. 

```
let str = 'Hello World!';
let lastChar = str.charAt(str.length - 1);
console.log(lastChar);
// Output: !
```

#2 Using the slice() Method

The slice() method is another built-in JavaScript string method that allows us to get a part of a string. To get the last character of a string, we can use the slice() method with the string's length minus one as the starting index argument and the string's length as the ending index argument. 

```
let str = 'Hello World!';
let lastChar = str.slice(str.length - 1);
console.log(lastChar);
// Output: !
```

#3 Using the substring() Method

The substring() method is another built-in JavaScript string method that allows us to get a part of a string. To get the last character of a string, we can use the substring() method with the string's length minus one as the starting index argument and the string's length as the ending index argument. 

```
let str = 'Hello World!';
let lastChar = str.substring(str.length - 1);
console.log(lastChar);
// Output: !
```

#4 Using the substr() Method

The substr() method is another built-in JavaScript string method that allows us to get a part of a string. To get the last character of a string, we can use the substr() method with the string's length minus one as the starting index argument and one as the length argument. 

```
let str = 'Hello World!';
let lastChar = str.substr(str.length - 1, 1);
console.log(lastChar);
// Output: !
```

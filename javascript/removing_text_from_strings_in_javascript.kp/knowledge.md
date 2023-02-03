---
title: What is the process for deleting characters from a string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the replace() method to remove text from a string in Javascript.
---

**Contents**

[TOC]

1. Using the `replace()` Method

The `replace()` method can be used to replace a specified value in a string with a new value. It can be used to remove text from a string by replacing the text with an empty string.

Syntax:

```
string.replace(valueToReplace, newValue)
```

Example:

```
var str = "Hello World!";
var res = str.replace("World", "");

console.log(res); // Outputs "Hello!"
```

2. Using the `split()` Method

The `split()` method can be used to split a string into an array of substrings based on a specified separator. It can be used to remove text from a string by splitting the string on the text to be removed and then joining the resulting array back into a string.

Syntax:

```
string.split(separator)
```

Example:

```
var str = "Hello World!";
var res = str.split("World").join("");

console.log(res); // Outputs "Hello!"
```

3. Using the `substring()` Method

The `substring()` method can be used to extract a part of a string between two specified indices. It can be used to remove text from a string by specifying the start index of the text to remove and the end index of the text to remove.

Syntax:

```
string.substring(startIndex, endIndex)
```

Example:

```
var str = "Hello World!";
var res = str.substring(0, 5);

console.log(res); // Outputs "Hello"
```

4. Using the `slice()` Method

The `slice()` method can be used to extract a part of a string between two specified indices. It can be used to remove text from a string by specifying the start index of the text to remove and the end index of the text to remove.

Syntax:

```
string.slice(startIndex, endIndex)
```

Example:

```
var str = "Hello World!";
var res = str.slice(0, 5);

console.log(res); // Outputs "Hello"
```

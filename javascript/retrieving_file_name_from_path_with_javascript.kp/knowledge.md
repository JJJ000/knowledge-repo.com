---
title: What is the JavaScript code to extract the file name from a full path?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `path.basename()` method to get the file name from a full path using JavaScript.
---

**Contents**

[TOC]

## Section 1: Using the Split Method 
The split() method is used to split a string into an array of substrings, and returns the new array.

Syntax:
string.split(separator, limit)

Example:

```javascript
var path = "C:\\folder1\\folder2\\myfile.txt";
var fileName = path.split("\\").pop();
console.log(fileName);
// Output: myfile.txt
```

## Section 2: Using the Substring Method
The substring() method is used to extract the characters from a string, between two specified indices, and returns the new sub string.

Syntax:
string.substring(indexStart, indexEnd)

Example:

```javascript
var path = "C:\\folder1\\folder2\\myfile.txt";
var fileName = path.substring(path.lastIndexOf("\\") + 1);
console.log(fileName);
// Output: myfile.txt
```

## Section 3: Using the Match Method
The match() method is used to search a string for a match against a regular expression, and returns the matches, as an Array object.

Syntax:
string.match(regexp)

Example:

```javascript
var path = "C:\\folder1\\folder2\\myfile.txt";
var fileName = path.match(/[^\\]+$/)[0];
console.log(fileName);
// Output: myfile.txt
```

## Section 4: Using the Replace Method
The replace() method is used to search a string for a specified value, or a regular expression, and returns a new string where the specified values are replaced.

Syntax:
string.replace(searchvalue, newvalue)

Example:

```javascript
var path = "C:\\folder1\\folder2\\myfile.txt";
var fileName = path.replace(/.*[\\\/]/, '');
console.log(fileName);
// Output: myfile.txt
```

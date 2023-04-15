---
title: What is the best way to replace all instances of a string in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the String.prototype.replace() method.
---

**Contents**

[TOC]

**Solution 1: Using the replace() Method**

The `replace()` method can be used to replace all occurrences of a specified string in a given string. It takes two parameters: the string to be replaced and the string to replace it with.

Syntax:

```
string.replace(oldString, newString);
```

Example:

```
var str = "This is a test string";
str = str.replace("test", "new");
// str = "This is a new string"
```

**Solution 2: Using Regular Expressions**

Regular expressions can be used to replace all occurrences of a specified string in a given string. The `replace()` method can be used with a regular expression to replace all occurrences of a specified string.

Syntax:

```
string.replace(/oldString/g, newString);
```

Example:

```
var str = "This is a test string";
str = str.replace(/test/g, "new");
// str = "This is a new string"
```

**Solution 3: Using a Loop**

A loop can be used to replace all occurrences of a specified string in a given string. The loop can iterate through the string and replace each occurrence of the specified string with the new string.

Example:

```
var str = "This is a test string";
var newStr = "";
for (var i = 0; i < str.length; i++) {
  if (str[i] === "test") {
    newStr += "new";
  } else {
    newStr += str[i];
  }
}
// newStr = "This is a new string"
```

**Solution 4: Using the split() and join() Methods**

The `split()` and `join()` methods can be used to replace all occurrences of a specified string in a given string. The `split()` method can be used to split the string into an array of strings, and then the `join()` method can be used to join the array of strings back into a string with the specified string replaced.

Syntax:

```
string.split(oldString).join(newString);
```

Example:

```
var str = "This is a test string";
str = str.split("test").join("new");
// str = "This is a new string"
```

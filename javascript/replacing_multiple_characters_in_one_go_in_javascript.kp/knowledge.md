---
title: Substitute multiple characters in a single replace operation
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, it is possible to replace multiple characters in one replace call in Javascript by using a regular expression.
---

**Contents**

[TOC]

**Section 1: Using Regular Expressions**

Using regular expressions, you can replace multiple characters in one replace call by including them in the regex pattern. For example, the following code will replace all instances of the characters 'a', 'b', and 'c' in a string:

```
var myString = "abcdefg";
myString = myString.replace(/[abc]/g, "");
```

The `g` flag is used to make sure that all instances of the characters are replaced, not just the first one.

**Section 2: Using String.prototype.replace**

If you don't want to use regular expressions, you can also use the `String.prototype.replace` method to replace multiple characters in one call. This method takes two arguments: a string containing the characters to be replaced, and a string containing the replacement characters. For example, the following code will replace all instances of the characters 'a', 'b', and 'c' in a string:

```
var myString = "abcdefg";
myString = myString.replace("abc", "");
```

**Section 3: Using Array.prototype.join**

You can also use the `Array.prototype.join` method to replace multiple characters in one call. This method takes an array of characters to be replaced and joins them into a single string. For example, the following code will replace all instances of the characters 'a', 'b', and 'c' in a string:

```
var myString = "abcdefg";
myString = myString.replace(["a", "b", "c"].join(""), "");
```

**Section 4: Using String.prototype.split**

The `String.prototype.split` method can also be used to replace multiple characters in one call. This method takes a string containing the characters to be replaced and splits them into an array. For example, the following code will replace all instances of the characters 'a', 'b', and 'c' in a string:

```
var myString = "abcdefg";
myString = myString.replace(myString.split(""), "");
```

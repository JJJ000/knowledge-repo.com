---
title: Transforming a user-entered string into a regular expression
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the RegExp constructor to convert a user input string into a regular expression in Javascript.
---

**Contents**

[TOC]

# Section 1: Understanding Regular Expressions
Regular expressions (often referred to as "regex") are a powerful tool used to match patterns in strings. They are composed of characters that have special meaning and are used to match one or more characters in a string. Regular expressions can be used to search, edit, and manipulate text.

# Section 2: Converting a String to a Regular Expression
In Javascript, a string can be converted to a regular expression using the RegExp constructor. The constructor takes a string as an argument, which can be a literal string or a string containing a regular expression pattern. 

# Section 3: Example
For example, if you want to create a regular expression that matches the words "cat" or "dog", you can use the following code:

```javascript
var regex = new RegExp("\\b(cat|dog)\\b");
```

# Section 4: Using User Input
You can also use user input to create a regular expression. To do this, you will need to first sanitize the user input to make sure it does not contain any malicious code. Once the input is sanitized, you can use the same RegExp constructor to create a regular expression from the user input. 

For example, if the user input is "cat|dog", you can use the following code to create a regular expression that matches the words "cat" or "dog":

```javascript
var userInput = "cat|dog";
var regex = new RegExp(userInput);
```

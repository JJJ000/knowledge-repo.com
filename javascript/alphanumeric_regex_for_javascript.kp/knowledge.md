---
title: A regular expression for JavaScript that allows only alphanumeric characters
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The regular expression for allowing only alphanumeric in Javascript is /^[a-z0-9]+$/i.
---

**Contents**

[TOC]

1. **Definition**
A regular expression (RegEx) is a sequence of characters that define a search pattern used for finding and matching specific strings of text.

2. **Creating a RegEx for Alphanumeric**
The RegEx for allowing only alphanumeric characters can be created using the following pattern:

`/^[a-zA-Z0-9]*$/`

3. **Explaining the Pattern**
The pattern starts with a forward slash (/) and a caret (^) symbol, which tells the RegEx engine to start matching from the beginning of the string. The square brackets ([]) define a character class, which allows only the characters inside the brackets to be matched. In this case, the character class contains lowercase letters (a-z), uppercase letters (A-Z), and numbers (0-9). The asterisk (*) symbol is a quantifier that specifies that the characters in the character class can be matched zero or more times. Finally, the pattern ends with a forward slash (/) and a dollar sign ($), which tells the RegEx engine to match only until the end of the string.

4. **Using the RegEx in Javascript**
The RegEx can be used in Javascript to check if a string contains only alphanumeric characters by using the `test()` method. For example:

`var regex = /^[a-zA-Z0-9]*$/;
var string = "abc123";

if (regex.test(string)) {
  console.log("The string contains only alphanumeric characters");
} else {
  console.log("The string contains non-alphanumeric characters");
}`

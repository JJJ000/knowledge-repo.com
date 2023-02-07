---
title: What is the process for applying a JavaScript regular expression across multiple lines?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `m` (multiline) flag when creating the regex to allow it to span multiple lines.
---

**Contents**

[TOC]

### Section 1: Using the Regex Literal

The easiest way to use a JavaScript regex over multiple lines is to use the regex literal. The regex literal is a way of defining a regex pattern in JavaScript without having to use the `RegExp` constructor. It is written as a regular string with the addition of forward slashes (`/`) at the beginning and end of the pattern. For example: 

```js
const regex = /^[a-z]\w+$/;
```

To use a regex literal over multiple lines, you can use the backslash (`\`) character at the end of each line to indicate that the regex pattern continues on the next line. For example:

```js
const regex = /^[a-z]\w+$
               \s+$/;
```

### Section 2: Using the RegExp Constructor

If you are not able to use a regex literal, then you can use the `RegExp` constructor to create a regex pattern. The `RegExp` constructor takes two parameters: a string containing the pattern and an optional string containing the flags. To use a regex pattern over multiple lines, you must use the `RegExp` constructor and pass in a string containing the pattern. For example:

```js
const regex = new RegExp(
  "^[a-z]\\w+$\n" +
  "\\s+$"
);
```

### Section 3: Escaping Characters

When using a regex pattern over multiple lines, it is important to remember to escape any special characters that may be present in the pattern. For example, the backslash (`\`) character must be escaped when using a regex literal. For example:

```js
const regex = /^[a-z]\\w+$
               \s+$/;
```

When using the `RegExp` constructor, the backslash (`\`) character must be escaped twice. For example:

```js
const regex = new RegExp(
  "^[a-z]\\\\w+$\n" +
  "\\\\s+$"
);
```

### Section 4: Testing the Pattern

Once you have created your regex pattern, it is important to test it to ensure that it works as expected. You can use the `test()` method of the `RegExp` object to test a string against the pattern. For example:

```js
const regex = /^[a-z]\w+$\s+$/;
const str = "myString   ";

const result = regex.test(str);
// result is true
```

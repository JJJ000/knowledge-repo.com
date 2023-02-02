---
title: What is the syntax for incorporating a variable into a regular expression?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use a variable in a regular expression by enclosing it in forward slashes, such as /variableName/.
---

**Contents**

[TOC]

### Using a Variable

To use a variable in a regular expression in Javascript, the variable must first be declared. The variable can be declared using either `let` or `const`, depending on the desired scope of the variable. 

Once the variable is declared, it can be used inside of the regular expression. This is done by enclosing the variable within a set of parentheses and preceding it with a backslash. 

### Example

For example, let's say we have a variable `name` declared as follows:

```javascript
let name = "John";
```

We can use this variable in a regular expression as follows:

```javascript
let regex = new RegExp(`Hello, \\${name}!`);
```

This regular expression will match the string `Hello, John!`.

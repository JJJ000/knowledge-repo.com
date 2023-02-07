---
title: What is the reason for jshint displaying a warning when I use the 'const' keyword?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: JSHint throws a warning when using const because it is not supported in all browsers.
---

**Contents**

[TOC]

# Explanation
JSHint is a static code analysis tool used in software development for checking if JavaScript source code complies with coding rules. It is designed to detect potential problems in JavaScript code that may lead to errors. It can also detect certain coding conventions that may be considered bad practice.

# Warning with Const
The warning thrown by JSHint when using the keyword const is because const is a relatively new feature in the JavaScript language. It was introduced in ES6, so not all browsers support it yet. As a result, JSHint will warn you if you are using const since it may not work in all browsers.

# Solution
The solution to this warning is to use a transpiler such as Babel or TypeScript to convert the code from ES6 to ES5, which is supported by all browsers. This will allow you to use const without any warnings from JSHint.

# Conclusion
In conclusion, JSHint throws a warning when using const because it is not supported by all browsers yet. The solution is to use a transpiler to convert the code from ES6 to ES5, which is supported by all browsers.

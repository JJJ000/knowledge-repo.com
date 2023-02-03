---
title: The regeneratorruntime variable is not defined in babel 6
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Babel 6 does not automatically include the regeneratorRuntime, so it must be imported manually.
---

**Contents**

[TOC]

# Overview
Babel 6 is a JavaScript compiler that allows users to write code using the latest version of JavaScript, and then compile it into a version that is supported by most browsers. One of the features of Babel 6 is the ability to use the latest version of the JavaScript language, which includes the "regeneratorRuntime" feature. Unfortunately, this feature is not defined in the JavaScript language, and as a result, it can cause errors when trying to compile code using Babel 6.

# What is regeneratorRuntime?
RegeneratorRuntime is a feature of the latest version of JavaScript that allows users to write asynchronous code. It provides a way for users to write code that will run in the background, without blocking other parts of the program. This is especially useful when writing code that needs to wait for an API call to return data, or when writing code that needs to run after a certain amount of time has passed.

# Why is regeneratorRuntime not defined in JavaScript?
The reason why regeneratorRuntime is not defined in the JavaScript language is because it is a feature of the latest version of JavaScript, and not all browsers support this version. As a result, browsers that do not support the latest version of JavaScript will not recognize the regeneratorRuntime feature, and will throw an error when trying to compile code that uses it.

# How to fix this issue?
Fortunately, there is a way to fix this issue. By using a polyfill, users can add the regeneratorRuntime feature to their code, allowing it to be compiled correctly in browsers that do not support the latest version of JavaScript. A polyfill is a piece of code that adds support for a feature that is not supported by a particular browser. In this case, the polyfill adds the regeneratorRuntime feature to the code, allowing it to be compiled correctly.

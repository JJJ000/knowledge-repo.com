---
title: Comparing the differences between json.parse and eval()
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON.parse is a safer and more secure way to parse JSON data than eval(), as it does not execute code and does not allow access to the global scope.
---

**Contents**

[TOC]

### JSON.parse

JSON.parse is a built-in method of the JavaScript global object JSON for parsing a JSON string. It takes a JSON string and returns a JavaScript object or array containing the parsed data.

### Advantages

JSON.parse is considered safer to use than eval() because it does not execute arbitrary code. It also allows for more efficient data structures than eval(), since it does not need to parse the entire string.

### Disadvantages

JSON.parse is slower than eval() since it needs to parse the entire string. It also does not support comments, which can make debugging difficult.

### eval()

eval() is a JavaScript function that evaluates a string of JavaScript code and executes it. It can take a string of JavaScript code and execute it, allowing for the dynamic execution of code.

### Advantages

eval() is faster than JSON.parse since it only needs to parse the code it is given. It also supports comments, which can make debugging easier.

### Disadvantages

eval() is considered less secure than JSON.parse since it can execute arbitrary code. It also does not allow for more efficient data structures than JSON.parse, since it needs to parse the entire string.

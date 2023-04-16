---
title: What are the guidelines for javascript's automatic semicolon insertion (asi)?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JavaScript will automatically insert semicolons at the end of a line if the line does not contain any semicolon and the next line does not start with a curly brace.
---

**Contents**

[TOC]

## 1. Statements

JavaScript's automatic semicolon insertion (ASI) is a feature that allows the interpreter to automatically insert a semicolon at the end of a line if it is missing. This allows for cleaner code and fewer syntax errors.

ASI will insert a semicolon when it sees a line break after a statement. This means that a statement must be terminated with a semicolon in order for ASI to work properly.

## 2. Expressions

ASI will not insert a semicolon when it sees a line break after an expression. This means that expressions must not be terminated with a semicolon in order for ASI to work properly.

## 3. Loops and Blocks

ASI will not insert a semicolon after a loop or a block of code. This means that loops and blocks must be terminated with a semicolon in order for ASI to work properly.

## 4. Return Statements

ASI will not insert a semicolon after a return statement. This means that return statements must be terminated with a semicolon in order for ASI to work properly.

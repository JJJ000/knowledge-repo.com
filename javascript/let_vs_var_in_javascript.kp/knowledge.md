---
title: How do 'let' and 'var' differ?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: `Let` is a block-scoped variable, while `var` is a function-scoped variable.
---

**Contents**

[TOC]

### Definition

**let**: The let keyword is used to declare a block-scoped local variable, optionally initializing it to a value.

**var**: The var keyword is used to declare a local or global variable, optionally initializing it to a value.

### Scope

**let**: Variables declared with let are scoped to the nearest enclosing block.

**var**: Variables declared with var are scoped to the nearest function block.

### Re-declaration

**let**: Variables declared with let can be re-declared within the same scope.

**var**: Variables declared with var can be re-declared within the same scope.

### Hoisting

**let**: Variables declared with let are not hoisted to the top of the block.

**var**: Variables declared with var are hoisted to the top of the block.

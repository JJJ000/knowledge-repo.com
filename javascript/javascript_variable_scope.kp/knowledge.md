---
title: What are the boundaries of where a variable can be accessed in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: In JavaScript, variables have either local or global scope, depending on where they are declared.
---

**Contents**

[TOC]

# Global Scope
Variables declared outside of any function are in the global scope and can be accessed from anywhere in the code.

# Function Scope
Variables declared within a function are in the local scope and can only be accessed within that function.

# Block Scope
Variables declared with the `let` and `const` keywords are in the block scope and can only be accessed within the block they were declared in.

# Lexical Scope
Variables declared in a higher scope are accessible in lower scopes. This means that if a variable is declared in the global scope, it can be accessed from within any function.

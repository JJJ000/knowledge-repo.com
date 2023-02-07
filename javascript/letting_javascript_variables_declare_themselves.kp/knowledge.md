---
title: What is the significance of the name 'let' for block-scoped variable declarations in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The name `let` was chosen for block-scoped variable declarations in JavaScript because it is a keyword that is already used in other programming languages to declare variables.
---

**Contents**

[TOC]

#### History

The keyword `let` was introduced in ES6 (ECMAScript 2015) as a way to declare block-scoped variables. Prior to ES6, variables declared with the `var` keyword were only function-scoped, meaning they could be accessed from anywhere within the same function.

#### Rationale

The choice of the keyword `let` was intentional, as it is a keyword in many other programming languages, including C, C++, Java, and Python. By using `let`, the JavaScript developers were able to make the language more familiar to developers coming from other programming languages.

#### Other Options

Prior to the introduction of `let`, other keywords were considered, such as `const`, `block`, and `varlet`. Ultimately, `let` was chosen because it was the most concise and least likely to cause confusion.

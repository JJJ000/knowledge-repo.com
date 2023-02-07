---
title: Do variables declared with let or const get moved to the top of the code when the program is run?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, variables declared with let or const are hoisted in Javascript.
---

**Contents**

[TOC]

## Yes

Variables declared with `let` and `const` are hoisted in Javascript. This means that they are available from the start of the scope in which they are declared, regardless of where they are declared in the code.

## No

However, variables declared with `let` and `const` are not initialized until they are declared. This means that they cannot be used before they are declared. If they are used before they are declared, an error will be thrown.

---
title: Comparing typeof with "undefined" versus not equal to null
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The operator `!==` checks for both type and value, while the operator `!= null` only checks for value.
---

**Contents**

[TOC]

### typeof !== "undefined"

The `typeof !== "undefined"` operator is used to determine if a variable has been declared and is not `undefined`. It is a strict comparison operator, meaning that it will not perform type coercion.

### != null

The `!= null` operator is used to determine if a variable is not `null`. It is a loose comparison operator, meaning that it will perform type coercion. This means that if a variable is declared as `null` but is of a different type, such as a number, the operator will still return `true`.

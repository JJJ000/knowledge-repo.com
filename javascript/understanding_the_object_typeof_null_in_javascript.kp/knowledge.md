---
title: What is the reason that the typeof null is "object"?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Because in the early days of Javascript, null was treated as an object, and the typeof operator was not updated to reflect this change.
---

**Contents**

[TOC]

# Historical Reasons

In the early days of JavaScript, the language was loosely typed and variables could be declared without a type. `null` was a special value that was used to denote an empty or non-existent value. As such, it was treated as an object.

# Lack of Reflection

JavaScript does not provide a built-in way to determine the type of an object. Instead, the `typeof` operator is used to determine the type of a value. Since `null` is an object, `typeof null` returns `object`.

# Inconsistency

The `typeof` operator is also inconsistent with other primitive values. For example, `typeof "string"` returns `string` and `typeof 1` returns `number`. This inconsistency makes it difficult for developers to remember the type of `null`.

# No Change

Due to the widespread use of `null` in JavaScript, changing the behavior of `typeof` to return `null` would break existing code. As such, the `typeof null` has remained `object` since the early days of JavaScript.

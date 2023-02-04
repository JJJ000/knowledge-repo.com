---
title: What is the meaning of 'void 0'?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Void 0 is an expression used to return undefined in Javascript.
---

**Contents**

[TOC]

# Definition

`void 0` is an expression in Javascript which evaluates to `undefined`.

# Usage

`void 0` is used to explicitly return `undefined` from a function. It is also used to suppress the value of an expression from being returned.

# Benefits

`void 0` is more concise than `undefined` and more reliable than `undefined` when used in certain contexts. It can also be used to avoid errors when `undefined` is a valid value.

# Examples

```
function foo() {
  return void 0;
}

const bar = (() => void 0)();

if (typeof baz !== void 0) {
  console.log('baz is defined');
}
```

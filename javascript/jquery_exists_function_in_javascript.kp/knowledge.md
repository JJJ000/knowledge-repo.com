---
title: Does jquery have a function called 'exists'?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, there is no `exists` function for jQuery in Javascript.
---

**Contents**

[TOC]

## Definition

The `exists()` function does not exist in jQuery or JavaScript.

## Alternatives

The `length` property of a jQuery object can be used to determine if the query yielded any results. If the length is 0, then no results were returned.

For example:

```javascript
if ($('#myElement').length) {
  // element exists
}
```

## Further Reading

For more information, see [this Stack Overflow post](https://stackoverflow.com/questions/31044/is-there-an-exists-function-for-jquery).

---
title: Is there a way in JavaScript to create a range of numbers between two given values?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, JavaScript does not have a built-in method like `range()` to generate a range within the supplied bounds.
---

**Contents**

[TOC]

### No

JavaScript does not have a method like `range()` to generate a range within the supplied bounds.

### Alternatives

However, there are other ways to generate a range within the supplied bounds. For example, a simple for loop can be used to iterate over a range of numbers:

```javascript
// Create an empty array
let rangeArray = [];

// Iterate over a range of numbers
for (let i = start; i <= end; i++) {
    rangeArray.push(i);
}
```

### Libraries

Alternatively, there are libraries such as [lodash](https://lodash.com/docs/4.17.15#range) and [underscore](http://underscorejs.org/#range) that provide a `range()` method to generate a range within the supplied bounds.

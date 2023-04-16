---
title: Creating random integers in JavaScript within a specified range
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Math.floor(Math.random() * (max - min + 1)) + min can be used to generate a random whole number in a specific range.
---

**Contents**

[TOC]

**Math.random() Method**

The Math.random() method can be used to generate a random whole number in a specific range. This method returns a random number between 0 (inclusive) and 1 (exclusive).

**Syntax**

The syntax for using the Math.random() method is as follows:

```
Math.random()
```

**Example**

The following example generates a random whole number between 1 and 10:

```
Math.floor(Math.random() * 10) + 1
```

**Result**

The result of the above example could be any number from 1 to 10.

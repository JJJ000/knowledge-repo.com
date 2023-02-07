---
title: Check if a string is present in a list in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To determine if a string is in a list, use the Array.prototype.includes() method.
---

**Contents**

[TOC]

**Using the `indexOf()` Method**

The `indexOf()` method can be used to determine if a string is in a list. This method returns the index of the first occurrence of the specified value in the list. If the value is not found, it returns -1.

**Syntax**

```
list.indexOf(value)
```

**Example**

```
let list = ["apple", "banana", "orange"];
let value = "banana";

list.indexOf(value);
// Output: 1
```

**Using the `includes()` Method**

The `includes()` method can also be used to determine if a string is in a list. This method returns a boolean value (true or false) depending on whether the specified value is found in the list.

**Syntax**

```
list.includes(value)
```

**Example**

```
let list = ["apple", "banana", "orange"];
let value = "banana";

list.includes(value);
// Output: true
```

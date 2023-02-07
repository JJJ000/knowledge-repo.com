---
title: Using const correctly when defining functions
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: When defining functions in Javascript, const should be used to ensure that the function cannot be reassigned.
---

**Contents**

[TOC]

### Definition 
Const is a keyword in JavaScript used to declare a constant. A constant is a variable that cannot be re-assigned a value.

### Usage 
When defining functions in JavaScript, const can be used to create a constant reference to a function. This ensures that the function cannot be reassigned to a different value.

### Example

```
const myFunction = () => {
  // Function code here
};
```

### Benefits
Using const for defining functions in JavaScript offers the following benefits: 
- Ensures that the function cannot be reassigned
- Improves code readability
- Improves code maintainability

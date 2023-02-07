---
title: What is the process for determining if a variable has a value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `!==` operator to check if a variable is not null in Javascript.
---

**Contents**

[TOC]

# Using the Equality Operator

The equality operator `==` can be used to check if a variable is not null.

```javascript
if(variableName != null){
  // code
}
```

# Using the Strict Equality Operator

The strict equality operator `===` can be used to check if a variable is not null.

```javascript
if(variableName !== null){
  // code
}
```

# Using the Typeof Operator

The typeof operator can be used to check if a variable is not null.

```javascript
if(typeof variableName !== "undefined"){
  // code
}
```

# Using the Undefined Property

The undefined property can be used to check if a variable is not null.

```javascript
if(variableName !== undefined){
  // code
}
```

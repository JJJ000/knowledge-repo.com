---
title: Verify if a value is present in an enumeration in typescript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, you can use the `in` operator to check if a value exists in an enum in TypeScript.
---

**Contents**

[TOC]

**Section 1: Overview**
Enums in TypeScript are a way to define a set of named constants. They can be used to create type-safe code, as they allow you to limit the range of values that a variable can take on. In this article, we will explore how to check if a value exists in an enum in TypeScript.

**Section 2: Using the ‘in’ Operator**
The easiest way to check if a value exists in an enum in TypeScript is to use the ‘in’ operator. This operator takes a value and checks if it is present in an enum. It returns a boolean, so you can use it in a conditional statement. For example:

```
enum MyEnum {
  Value1,
  Value2,
  Value3
}

let myValue = "Value1";

if (myValue in MyEnum) {
  console.log("Value exists in enum!");
}
```

**Section 3: Using the ‘hasOwnProperty’ Method**
Another way to check if a value exists in an enum in TypeScript is to use the ‘hasOwnProperty’ method. This method takes a value and checks if it is present in an enum. It returns a boolean, so you can use it in a conditional statement. For example:

```
enum MyEnum {
  Value1,
  Value2,
  Value3
}

let myValue = "Value1";

if (MyEnum.hasOwnProperty(myValue)) {
  console.log("Value exists in enum!");
}
```

**Section 4: Conclusion**
In this article, we explored two different ways to check if a value exists in an enum in TypeScript. The ‘in’ operator and the ‘hasOwnProperty’ method both take a value and check if it is present in an enum. They both return a boolean, so you can use them in a conditional statement.

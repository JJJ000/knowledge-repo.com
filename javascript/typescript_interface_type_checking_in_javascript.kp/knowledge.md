---
title: Verifying the compatibility of interfaces using typescript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Typescript can be used to add type checking to JavaScript code to ensure that variables are used correctly.
---

**Contents**

[TOC]

## Introduction
TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. It offers classes, modules, and interfaces to help you build robust components. TypeScript is designed for the development of large applications and transcompiles to JavaScript.

## TypeScript Interfaces
An interface in TypeScript is a syntactical contract that an entity should conform to. In other words, an interface defines the syntax that any entity must adhere to.

Interfaces define properties, methods, and events, which are the members of the interface. Interfaces contain only the declaration of the members but not the implementation. It is the responsibility of the deriving class to define the members.

## TypeScript Interface Checking
TypeScript provides static type-checking on both the interface level and the variable level. TypeScript uses the same syntax as JavaScript, with types after the variable name.

For example, if you have an interface called "Person" that contains the properties "name" and "age", you can declare a variable of type "Person" and assign it a value that conforms to the structure of the interface:

```
let person: Person = {
    name: "John",
    age: 25
};
```

If you try to assign a value to the variable that doesn't conform to the interface, TypeScript will throw an error.

## Conclusion
TypeScript interfaces are a great way to ensure that your code conforms to a specific structure. They can be used to define the structure of objects, classes, functions, and more. TypeScript also provides static type-checking to ensure that your code is valid and follows the interface definition.

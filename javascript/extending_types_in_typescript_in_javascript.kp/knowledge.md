---
title: Can additional types be added to typescript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, it is possible to extend types in Typescript by using the `extends` keyword.
---

**Contents**

[TOC]

## Yes
Typescript is a superset of Javascript, meaning that all valid Javascript code is valid Typescript code. This means that it is possible to extend types in Typescript, as any valid Javascript code can be used in Typescript.

## How
Typescript provides a number of ways to extend types. The most common way is to use the `interface` keyword to create a new type. This type can then be used to extend existing types.

For example, the following code creates a new type, `MyType`, which extends the built-in `Number` type:

```typescript
interface MyType extends Number {
  myProp: string;
}
```

This type can then be used to extend existing types, such as the built-in `Number` type:

```typescript
let x: MyType = 5;
x.myProp = "hello";
```

## Other Ways
In addition to the `interface` keyword, Typescript also provides other ways to extend types. These include the `type` keyword, the `class` keyword, and the `enum` keyword.

For example, the `type` keyword can be used to extend a type by creating a new type alias:

```typescript
type MyType = Number & { myProp: string };
```

The `class` keyword can be used to extend a type by creating a new class that inherits from an existing type:

```typescript
class MyType extends Number {
  myProp: string;
}
```

Finally, the `enum` keyword can be used to extend a type by creating a new enumeration:

```typescript
enum MyType {
  VALUE1 = "value1",
  VALUE2 = "value2"
}
```

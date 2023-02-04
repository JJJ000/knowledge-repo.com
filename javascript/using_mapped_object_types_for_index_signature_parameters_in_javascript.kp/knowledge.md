---
title: It is not possible to use a union type as a parameter type for an index signature. instead, try using a mapped object type
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: A mapped object type can be used instead of a union type as an index signature parameter type in Javascript.
---

**Contents**

[TOC]

### Introduction
An index signature parameter type is a type annotation that specifies the type of a property in an object. It is used in JavaScript to provide additional type information when accessing properties of an object. The type of the parameter can be a primitive type, a class, an interface, or an array type. However, a union type is not allowed as a parameter type for an index signature.

### Mapped Object Types
Mapped object types are a way to provide type information for objects in JavaScript. They are similar to index signatures, but they allow for more flexibility. With mapped object types, you can define the type of a property as a union type, which is not allowed with index signatures.

### Benefits of Mapped Object Types
Mapped object types provide more flexibility when defining the type of a property in an object. With a union type, you can specify multiple types for a property, which is not possible with index signatures. Additionally, mapped object types allow for more complex types, such as functions, which cannot be specified with index signatures.

### Conclusion
Index signatures are a great tool for providing type information for objects in JavaScript. However, if you need to specify a union type for a property, then mapped object types are the way to go. They provide more flexibility and allow for more complex types.

---
title: Could you explain what pecs (producer extends consumer super) is?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: PECS is a Java programming concept which states that a producer should be able to extend (produce) and a consumer should be able to consume, while the superclass defines the general behavior.
---

**Contents**

[TOC]

### Introduction

PECS (Producer Extends Consumer Super) is a design pattern used in Java programming. It is used to create a type-safe and flexible API for a library or framework. The pattern is based on the concept of generics, which allows a type to be parameterized when defining classes, interfaces, and methods.

### How PECS Works

PECS works by defining two type parameters, one for the producer and one for the consumer. The producer type is defined as an "extends" type, while the consumer type is defined as a "super" type. This means that the producer is allowed to produce any subtype of the specified type, while the consumer is only allowed to consume the specified type or any of its supertypes.

### Benefits of PECS

The main benefit of using PECS is that it allows for a type-safe and flexible API. By using generics, the API can be parameterized to accept any type of object, while still ensuring that the types are compatible. This makes it easier to maintain and extend the API as new types are added.

Additionally, PECS helps to prevent errors by ensuring that the types used in the API are compatible. This reduces the need for manual type checking and makes it easier to debug any errors that may occur.

### Conclusion

PECS is a powerful design pattern that can be used to create a type-safe and flexible API for a library or framework. By using generics, it allows for a parameterized type system that ensures that the types used in the API are compatible. This reduces the need for manual type checking and makes it easier to maintain and extend the API.

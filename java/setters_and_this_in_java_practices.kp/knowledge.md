---
title: Is it considered poor form to have a setter return 'this'?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, it is not bad practice to make a setter return `this` in Java.
---

**Contents**

[TOC]

## Pros

Making a setter return "this" can be beneficial in certain cases as it allows for method chaining. This can make code more concise and readable. For example, when setting multiple properties of an object, it may be easier to write `object.setProperty1().setProperty2().setProperty3()` rather than `object.setProperty1(); object.setProperty2(); object.setProperty3();`.

## Cons

Using a setter that returns "this" is not always the most appropriate approach. This is because it can lead to confusion over the purpose of the method. It is not always clear that the method is intended to modify the object and not return a new value. Additionally, it can make it difficult to debug code as it is not always immediately evident which methods are being called and in what order.

## Alternatives

An alternative approach to using setters that return "this" is to use the builder pattern. This involves creating a separate class specifically for constructing objects with multiple properties. This class will have methods for setting each of the properties, but instead of returning "this" they will return the builder object. Once all of the properties have been set, the builder object can then be used to create the desired object.

## Conclusion

Making a setter return "this" can be beneficial in certain cases, but it is not always the most appropriate approach. Alternatives such as the builder pattern can provide a more robust and understandable way of constructing objects with multiple properties.

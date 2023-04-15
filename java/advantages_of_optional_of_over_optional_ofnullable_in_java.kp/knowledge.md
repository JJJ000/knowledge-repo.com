---
title: What are the benefits of using optional.of instead of optional.ofnullable?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Optional.of should be used when the value is known to be non-null, as it will throw a NullPointerException if a null value is provided.
---

**Contents**

[TOC]

#Advantages of Optional.of

1. Type Safety: Optional.of() provides type safety by ensuring that the value passed to it is not null. This is useful when you want to ensure that no null values are passed to the method.

2. Performance: Optional.of() is faster than Optional.ofNullable() because it does not need to check for null values.

#Advantages of Optional.ofNullable

1. Flexibility: Optional.ofNullable() allows you to pass in either a null or a non-null value. This is useful when you want to provide flexibility in the method call.

2. Error Handling: Optional.ofNullable() allows you to handle errors gracefully by catching null values and providing an alternative value. This is useful when you want to provide an alternative value when the original value is null.

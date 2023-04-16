---
title: What happens to Java generics during type erasure and when does it occur?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Generics type erasure occurs at compile time and replaces all generic type parameters and type arguments with their bounds or Object if the type parameter is unbounded.
---

**Contents**

[TOC]

#### What Is Generics Type Erasure

Generics type erasure is a process in Java where the generic type information is removed from the compiled code. This means that the type information is only available at compile time, and is not available at runtime. This is done to maintain backward compatibility with older versions of Java, as the original version of Java did not support generics.

#### When Does Generics Type Erasure Occur

Generics type erasure occurs during the compilation process. The compiler removes all type information associated with the generic type and replaces it with the type specified at compile time. This means that the type information is not available at runtime.

#### What Happens During Generics Type Erasure

During generics type erasure, the compiler removes all type information associated with the generic type and replaces it with the type specified at compile time. This means that the type information is not available at runtime, and all generic types are replaced with their raw types. For example, if a generic type of List<String> is specified, the compiler will replace it with List.

#### How Does Generics Type Erasure Affect Code

Generics type erasure can have a significant impact on code, as the type information is not available at runtime. This can lead to unexpected behaviors, as the compiler can replace generic types with their raw types. This can lead to errors, and can make debugging difficult. Additionally, it can make code harder to understand, as the type information is not available.

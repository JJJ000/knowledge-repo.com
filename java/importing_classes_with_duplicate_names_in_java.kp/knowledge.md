---
title: Rename the imported class in java, or import two distinct classes with the same name
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To import two classes with the same name, use the fully qualified class name.
---

**Contents**

[TOC]

1. **Renaming Imports**

It is possible to rename imports in Java. This is done by using the `import` keyword followed by the fully qualified name of the class, and then followed by the `as` keyword and the desired name for the import. For example, if you have imported a class called `Foo` from the package `com.example` and you want to refer to it as `Bar`, you would write the following:

```java
import com.example.Foo as Bar;
```

2. **Importing Two Classes with the Same Name**

It is not possible to import two classes with the same name. If you try to do so, the compiler will throw an error. The only way around this is to use a fully qualified name to refer to one of the classes, instead of using the imported name. For example, if you have two classes called `Foo` in two different packages, you can refer to one of them as follows:

```java
import com.example.Foo;
// ...
com.example.Foo foo = new com.example.Foo();
```

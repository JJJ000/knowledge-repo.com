---
title: What is the distinction between 'text' and a new string object created with the value 'text'?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The difference between `text` and new String(`text`) in Java is that `text` is a primitive string literal, while new String(`text`) is an object.
---

**Contents**

[TOC]

#### Constructors
"text" is a string literal, which is a primitive data type in Java. new String("text") is an object of type String, created by calling the String class constructor.

#### Memory Allocation
"text" is allocated memory on the stack, while new String("text") is allocated memory on the heap.

#### Mutability
"text" is immutable, meaning its value cannot be changed. new String("text") is mutable, meaning its value can be changed.

#### Garbage Collection
"text" is automatically garbage collected when the scope in which it was declared ends. new String("text") is not automatically garbage collected and must be manually garbage collected by the program.

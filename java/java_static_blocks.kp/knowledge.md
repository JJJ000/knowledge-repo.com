---
title: Reformulating "static block in java"
java's static block code
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A static block in Java is a block of code that is executed when a class is first loaded into memory.
---

**Contents**

[TOC]

### What is a Static Block?
A static block is a block of code or group of statements that are executed only once when the class is loaded into the memory. It is also known as a static initialization block.

### Syntax
The syntax of a static block is as follows:

```java
static {
    // code goes here
}
```

### Usage
Static blocks are used to initialize static variables. They can also be used to perform certain operations before the execution of the program starts.

### Example

For example, consider the following class:

```java
public class Example {
    public static int num;
 
    static {
        num = 10;
    }
 
    public static void main(String[] args) {
        System.out.println(num);
    }
}
```

In this example, the static block is used to initialize the static variable num to 10. When the program is executed, the output will be 10.

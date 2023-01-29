---
title: What is the syntax for including a reference to a method parameter in a javadoc comment?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Include the `@param` tag followed by the name and description of the parameter in the javadoc comment.
---

**Contents**

[TOC]

1. Overview
2. Syntax
3. Example

### Overview
Javadoc is a tool which generates documentation from Java source code. The documentation comments are specially formatted blocks of comments that are placed before class, fields, and methods. These comments are used to provide information about the code, such as the purpose of the method, its parameters, and the return type.

### Syntax
The syntax for adding a reference to a method parameter in javadoc is as follows:

`@param <parameter_name> <description>`

Where `<parameter_name>` is the name of the parameter and `<description>` is a description of the parameter.

### Example
For example, consider the following method:

```java
public void doSomething(int value) {
    // ...
}
```

The javadoc for this method might look like this:

```java
/**
 * Does something with the given value.
 * 
 * @param value The value to use.
 */
public void doSomething(int value) {
    // ...
}
```

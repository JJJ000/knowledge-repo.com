---
title: What is a lambda expression in Java 8 that can throw an exception?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A lambda function that throws an exception can be written as (args) -> { throw new Exception(); }.
---

**Contents**

[TOC]

### Syntax

```
(parameters) -> {
    throw exception;
}
```

### Example

```
(String s) -> {
    if(s == null) {
        throw new IllegalArgumentException("String cannot be null");
    }
}
```

### Usage

The following code snippet shows an example of how the lambda function can be used:

```
String input = null;
try {
    Consumer<String> consumer = (s) -> {
        if(s == null) {
            throw new IllegalArgumentException("String cannot be null");
        }
    };
    consumer.accept(input);
} catch (IllegalArgumentException e) {
    System.out.println(e.getMessage());
}
```

### Output

The output of the above code snippet is:

```
String cannot be null
```

---
title: What is the double colon operator in Java 8?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The double colon operator () in Java 8 is a shorthand notation for a method reference, which is used to refer to a method without invoking it.
---

**Contents**

[TOC]

### What is the :: (double colon) operator?
The double colon (::) operator is a new operator introduced in Java 8. It is also known as the method reference operator. The double colon operator allows a method or constructor reference to be passed as an argument to a method. It is used to refer to a method without actually invoking it.

### How is the :: (double colon) operator used?
The double colon operator is used to reference a method or constructor of a class. It is used in conjunction with a method reference or a constructor reference. When the double colon operator is used, the method or constructor reference is passed as an argument to the method.

### Examples
For example, consider the following code snippet:

```java
List<String> strings = Arrays.asList("a", "b", "c");
strings.forEach(System.out::println);
```

In this example, the double colon operator is used to reference the println method of the System class. The println method is then passed as an argument to the forEach method of the List class.

### Conclusion
The double colon (::) operator is a new operator introduced in Java 8. It is used to refer to a method or constructor of a class without actually invoking it. The double colon operator is used in conjunction with a method reference or a constructor reference. It is used to pass the method or constructor reference as an argument to a method.

---
title: What is the purpose of declaring a class as 'final' in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A final class in Java cannot be extended, meaning it cannot be used as a base class for other classes.
---

**Contents**

[TOC]

### Prevents Inheritance

The main purpose of a final class is to prevent the class from being extended. This means that any class that is declared as final cannot be extended by any other class. This can be useful in situations where the class needs to be kept immutable.

### Prevents Overriding

Another purpose of a final class is to prevent any of its methods from being overridden. This is useful when you want to ensure that the methods of a class are not changed in any way. It also helps to provide a level of security to the code, as it prevents any malicious code from being added to the class.

### Improved Performance

When a class is declared as final, the Java compiler can make certain optimizations to the code that can lead to improved performance. This is because the compiler can assume that the class will not be extended, and therefore can optimize the code accordingly.

### Security

Finally, declaring a class as final can also provide an extra layer of security to the code. This is because it prevents any malicious code from being added to the class, as the class cannot be extended. This can help to protect the code from any potential attacks.

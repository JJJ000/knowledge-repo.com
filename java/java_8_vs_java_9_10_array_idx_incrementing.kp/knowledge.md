---
title: What is the difference between Java 8 and Java 9/10 that causes array[idx++]+="a" to increase idx by one in Java 8 but by two in Java 9/10?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Java 9 and 10, the post-increment operator (++) has been changed to be evaluated before the addition operator (+=) instead of after, causing idx to be incremented twice.
---

**Contents**

[TOC]

### Introduction

The behavior of the expression `array[idx++]+="a"` has changed between Java 8 and Java 9 and 10. In Java 8, the expression increases `idx` by one, while in Java 9 and 10 it increases `idx` by two. This answer will explain the difference in behavior between the two versions of Java.

### Java 8

In Java 8, the expression `array[idx++]+="a"` is equivalent to the following two statements: 

```java
temp = array[idx]
array[idx] = temp + "a"
idx = idx + 1
```

Here, the value of `idx` is incremented after the array element has been modified.

### Java 9 and 10

In Java 9 and 10, the expression `array[idx++]+="a"` is equivalent to the following two statements: 

```java
temp = array[idx]
array[idx] = temp + "a"
idx = idx + 2
```

Here, the value of `idx` is incremented before the array element has been modified. This change was made to improve the performance of the expression.

### Conclusion

In conclusion, the behavior of the expression `array[idx++]+="a"` changed between Java 8 and Java 9 and 10. In Java 8, the expression increases `idx` by one, while in Java 9 and 10 it increases `idx` by two. This change was made to improve the performance of the expression.

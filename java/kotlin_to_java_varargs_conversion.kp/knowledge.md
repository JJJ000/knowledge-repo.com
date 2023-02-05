---
title: Transform a kotlin array into a Java variable arguments list
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Kotlin`s spread operator (`*`) can be used to convert an array to Java varargs.
---

**Contents**

[TOC]

# Section 1: Overview
Kotlin arrays can be converted to Java varargs using the `spread()` operator. The `spread()` operator allows for the elements of a Kotlin array to be passed as individual arguments to a Java method. 

# Section 2: Syntax
The syntax of the `spread()` operator is as follows: 

```
methodName(*arrayName.spread())
```

# Section 3: Example
For example, consider the following Kotlin array:

```
val array = arrayOf(1, 2, 3)
```

The `spread()` operator can be used to convert this array to a Java varargs as follows:

```
methodName(*array.spread())
```

# Section 4: Usage
The `spread()` operator can be used when calling Java methods from Kotlin. It allows for the elements of a Kotlin array to be passed as individual arguments to a Java method.

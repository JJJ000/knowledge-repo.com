---
title: What is the quickest method to check if the square root of an integer is a whole number?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Math.sqrt() method, and check if the result is equal to the floor of the result.
---

**Contents**

[TOC]

### Using Math.sqrt()

The `Math.sqrt()` method can be used to determine if the square root of an integer is an integer. This method takes a double as an argument and returns the square root of the argument as a double. To check if the returned double is an integer, we can compare the double to the result of casting the double as an integer. If the two values are equal, then the square root of the integer is an integer.

### Example

```java
public static boolean isSquareRootInteger(int x) {
    double sqrt = Math.sqrt(x);
    return sqrt == (int) sqrt;
}
```

### Time Complexity

The time complexity of this approach is O(1).

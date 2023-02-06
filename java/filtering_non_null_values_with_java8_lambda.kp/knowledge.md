---
title: Filter non-null values using a lambda expression in Java 8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the filter method with a lambda expression to filter the values if they are not null.
---

**Contents**

[TOC]

### Section 1: Overview

The purpose of this answer is to provide a solution for filtering values only if not null using lambda in Java 8.

### Section 2: Solution

The following code snippet provides a lambda expression that can be used to filter values only if not null:

```
list.stream()
    .filter(x -> x != null)
    .collect(Collectors.toList());
```

### Section 3: Explanation

The code snippet above uses the `filter()` method of the `Stream` class to filter out values that are not null. The `filter()` method takes a predicate as an argument which is used to evaluate each element of the stream. In this case, the predicate is `x -> x != null` which checks if the element is not null. The `collect()` method is then used to collect the filtered elements into a `List`.

### Section 4: Conclusion

In conclusion, the code snippet provided is a solution for filtering values only if not null using lambda in Java 8.

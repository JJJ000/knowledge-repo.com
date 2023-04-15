---
title: How to determine if a Java resultset contains any results?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the ResultSet`s next() method to check if there are any results.
---

**Contents**

[TOC]

1. Solution 1: Using `next()`
2. Solution 2: Using `getRow()`
3. Solution 3: Using `isBeforeFirst()`
4. Solution 4: Using `isAfterLast()`

### Solution 1: Using `next()`
The `ResultSet` interface provides the `next()` method which moves the cursor to the next row in the `ResultSet`. If the `ResultSet` contains no rows, the `next()` method returns `false`.

```java
if (rs.next()) {
    // There are results
} else {
    // No results
}
```

### Solution 2: Using `getRow()`
The `ResultSet` interface provides the `getRow()` method which returns the current row number in the `ResultSet`. If the `ResultSet` contains no rows, the `getRow()` method returns `0`.

```java
if (rs.getRow() > 0) {
    // There are results
} else {
    // No results
}
```

### Solution 3: Using `isBeforeFirst()`
The `ResultSet` interface provides the `isBeforeFirst()` method which checks if the cursor is before the first row in the `ResultSet`. If the `ResultSet` contains no rows, the `isBeforeFirst()` method returns `true`.

```java
if (!rs.isBeforeFirst()) {
    // There are results
} else {
    // No results
}
```

### Solution 4: Using `isAfterLast()`
The `ResultSet` interface provides the `isAfterLast()` method which checks if the cursor is after the last row in the `ResultSet`. If the `ResultSet` contains no rows, the `isAfterLast()` method returns `true`.

```java
if (!rs.isAfterLast()) {
    // There are results
} else {
    // No results
}
```

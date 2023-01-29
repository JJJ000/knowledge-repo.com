---
title: Change a boolean value to an integer in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Java, boolean values can be converted to int values by using the ternary operator (condition ? 1  0).
---

**Contents**

[TOC]

### Solution

### Method 1

Using the ternary operator:

```java
int i = booleanValue ? 1 : 0;
```

### Method 2

Using the Integer.valueOf() method:

```java
int i = Integer.valueOf(booleanValue);
```

### Method 3

Using the Integer.parseInt() method:

```java
int i = Integer.parseInt(String.valueOf(booleanValue));
```

### Method 4

Using the Boolean.compare() method:

```java
int i = Boolean.compare(booleanValue, false);
```

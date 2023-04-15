---
title: Change long to integer
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Long values can be converted to Integer values using the Long.intValue() method.
---

**Contents**

[TOC]

### Converting Long to Integer

1. Using `intValue()` Method: The `intValue()` method of the Long wrapper class can be used to convert a `Long` object to `Integer`. This method returns the value of this `Long` as an `int`.

Syntax: `longObject.intValue()`

Example:

```java
Long l = new Long(100);
Integer i = l.intValue();
System.out.println(i);
```

Output: `100`

2. Using `valueOf()` Method: The `valueOf()` method of the Integer wrapper class can be used to convert a `Long` object to `Integer`. This method returns an `Integer` object holding the value of the specified `Long` object.

Syntax: `Integer.valueOf(longObject)`

Example:

```java
Long l = new Long(100);
Integer i = Integer.valueOf(l);
System.out.println(i);
```

Output: `100`

3. Using `parseInt()` Method: The `parseInt()` method of the Integer wrapper class can be used to convert a `Long` object to `Integer`. This method returns an `Integer` object holding the value of the specified `Long` object.

Syntax: `Integer.parseInt(longObject.toString())`

Example:

```java
Long l = new Long(100);
Integer i = Integer.parseInt(l.toString());
System.out.println(i);
```

Output: `100`

4. Using `doubleValue()` Method: The `doubleValue()` method of the Long wrapper class can be used to convert a `Long` object to `Integer`. This method returns the value of this `Long` as a `double`.

Syntax: `longObject.doubleValue()`

Example:

```java
Long l = new Long(100);
int i = (int) l.doubleValue();
System.out.println(i);
```

Output: `100`

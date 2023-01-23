---
title: What is the process for obtaining an enumerated value from a string in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Use the `Enum.valueOf()` method to get an enum value from a string value in Java.
---

**Contents**

[TOC]

### Using valueOf() Method
The `valueOf()` method of the `Enum` class can be used to get the enum value from a string value.

### Syntax
The syntax for the `valueOf()` method is as follows:

`EnumName.valueOf(String value)`

### Example
Let's take an example of an enum `Day` with values `SUNDAY`, `MONDAY`, `TUESDAY`, etc.

To get the enum value from a string, we can use the `valueOf()` method as follows:

```java
Day day = Day.valueOf("SUNDAY");
```

### Output
The above code will set the `day` variable to `SUNDAY` enum value.

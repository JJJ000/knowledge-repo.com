---
title: What is the process for changing an integer to a long in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Long.valueOf() method to convert an int to a Long.
---

**Contents**

[TOC]

# Section 1: Using the Long Constructor 
You can use the Long constructor to convert an int to a Long. The syntax for the constructor is `Long(int)`. For example,

```java
int x = 10;
Long y = new Long(x);
```

# Section 2: Using the Long.valueOf Method
You can also use the Long.valueOf method to convert an int to a Long. The syntax for the method is `Long.valueOf(int)`. For example,

```java
int x = 10;
Long y = Long.valueOf(x);
```

# Section 3: Using the Long.parseLong Method
You can also use the Long.parseLong method to convert an int to a Long. The syntax for the method is `Long.parseLong(String)`. For example,

```java
int x = 10;
String s = String.valueOf(x);
Long y = Long.parseLong(s);
```

# Section 4: Using the Integer.toUnsignedLong Method
You can also use the Integer.toUnsignedLong method to convert an int to a Long. The syntax for the method is `Integer.toUnsignedLong(int)`. For example,

```java
int x = 10;
Long y = Integer.toUnsignedLong(x);
```

---
title: Change an integer to a string in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String.valueOf() method to convert an integer to a String.
---

**Contents**

[TOC]

### Method 1: Using String.valueOf()

The String.valueOf() method can be used to convert an integer to a String. It takes an integer argument and returns a String object representing the same value.

Syntax:
```
String.valueOf(int i)
```

Example:
```
int i = 10;
String str = String.valueOf(i);
```

### Method 2: Using Integer.toString()

The Integer.toString() method can be used to convert an integer to a String. It takes an integer argument and returns a String object representing the same value.

Syntax:
```
Integer.toString(int i)
```

Example:
```
int i = 10;
String str = Integer.toString(i);
```

### Method 3: Using String.format()

The String.format() method can be used to convert an integer to a String. It takes an integer argument and returns a String object representing the same value.

Syntax:
```
String.format("%d", int i)
```

Example:
```
int i = 10;
String str = String.format("%d", i);
```

### Method 4: Using StringBuilder

The StringBuilder class can be used to convert an integer to a String. It takes an integer argument and returns a String object representing the same value.

Syntax:
```
StringBuilder sb = new StringBuilder();
sb.append(int i);
String str = sb.toString();
```

Example:
```
int i = 10;
StringBuilder sb = new StringBuilder();
sb.append(i);
String str = sb.toString();
```

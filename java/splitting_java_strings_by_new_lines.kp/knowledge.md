---
title: Divide Java string by line break
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The String can be split using the split() method with `\n` as the delimiter.
---

**Contents**

[TOC]

### Using String.split() Method

This method splits a string into an array of substrings given a specific delimiter.

```java
String[] lines = str.split("\\r?\\n");
```

### Using Scanner

The Scanner class can be used to read a file line by line and store each line in an array.

```java
Scanner scanner = new Scanner(str); 
List<String> lines = new ArrayList<String>(); 
while (scanner.hasNextLine()) { 
    lines.add(scanner.nextLine()); 
} 
```

### Using StringTokenizer

The StringTokenizer class can be used to split a String into multiple tokens.

```java
StringTokenizer st = new StringTokenizer(str, "\n"); 
List<String> lines = new ArrayList<String>(); 
while (st.hasMoreTokens()) { 
    lines.add(st.nextToken()); 
} 
```

### Using Apache Commons

The StringUtils class from the Apache Commons library can be used to split a String.

```java
String[] lines = StringUtils.split(str, "\n");
```

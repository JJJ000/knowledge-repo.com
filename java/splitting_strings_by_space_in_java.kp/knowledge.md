---
title: What is the best way to divide a string by spaces?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the split() method of the String class, passing a space character (` `) as the delimiter.
---

**Contents**

[TOC]

`**` Import the String Class**

```java
import java.lang.String;
```

`**` Create a String Object**

```java
String str = "This is a string";
```

`**` Use the split() Method**

```java
String[] parts = str.split(" ");
```

`**` Print the Result**

```java
for (String part : parts) {
    System.out.println(part);
}
```

---
title: How can I change a certain character in a string at a particular position?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: StringBuilder sb = new StringBuilder(str); sb.setCharAt(index, newChar); str = sb.toString();
---

**Contents**

[TOC]

### Using StringBuilder

StringBuilder can be used to replace a character at a specific index in a string.

1. Create a StringBuilder object and pass the string as an argument.

```java
StringBuilder sb = new StringBuilder(str);
```

2. Use the `setCharAt()` method to replace the character at the specified index.

```java
sb.setCharAt(index, c);
```

3. Convert the StringBuilder back to a string using the `toString()` method.

```java
String newStr = sb.toString();
```

### Using Substring

Substring can be used to replace a character at a specific index in a string.

1. Create two substrings from the given string using the `substring()` method.

```java
String first = str.substring(0, index);
String second = str.substring(index + 1);
```

2. Concatenate the substrings with the desired character.

```java
String newStr = first + c + second;
```

3. The new string will contain the desired character at the specified index.

---
title: What is the procedure to delete the last character in a stringbuilder?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The last character of a StringBuilder can be removed using the deleteCharAt() method.
---

**Contents**

[TOC]

**Solution 1:**

Using `deleteCharAt()` Method

Step 1: Create a StringBuilder object.

```java
StringBuilder sb = new StringBuilder("Hello World");
```

Step 2: Use the `deleteCharAt()` method to delete the last character.

```java
sb.deleteCharAt(sb.length() - 1);
```

Step 3: Print the updated StringBuilder object.

```java
System.out.println(sb);
```

**Solution 2:**

Using `substring()` Method

Step 1: Create a StringBuilder object.

```java
StringBuilder sb = new StringBuilder("Hello World");
```

Step 2: Use the `substring()` method to create a new StringBuilder object without the last character.

```java
sb = new StringBuilder(sb.substring(0, sb.length() - 1));
```

Step 3: Print the updated StringBuilder object.

```java
System.out.println(sb);
```

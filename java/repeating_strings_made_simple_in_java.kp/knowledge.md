---
title: An easy method of repeating a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String.repeat() method.
---

**Contents**

[TOC]

**Using for loop:**

```java
public static String repeatString(String str, int times) {
    StringBuilder sb = new StringBuilder();
    for (int i = 0; i < times; i++) {
        sb.append(str);
    }
    return sb.toString();
}
```

**Using String.repeat():**

```java
public static String repeatString(String str, int times) {
    return str.repeat(times);
}
```

**Using StringUtils.repeat():**

```java
public static String repeatString(String str, int times) {
    return StringUtils.repeat(str, times);
}
```

**Using Apache Commons Lang:**

```java
public static String repeatString(String str, int times) {
    return org.apache.commons.lang3.StringUtils.repeat(str, times);
}
```

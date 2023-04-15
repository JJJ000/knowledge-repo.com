---
title: What is the process for determining the frequency of a character in a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.replaceAll() method to replace the character with an empty string, then use the length of the resulting string to count the number of occurrences.
---

**Contents**

[TOC]

**Solution 1: Using for loop**

```
public static int countOccurrences(String str, char c) {
    int count = 0;
    for (int i = 0; i < str.length(); i++) {
        if (str.charAt(i) == c) {
            count++;
        }
    }
    return count;
}
```

**Solution 2: Using Java 8 Stream API**

```
public static int countOccurrences(String str, char c) {
    return (int) str.chars().filter(ch -> ch == c).count();
}
```

**Solution 3: Using Apache Commons Lang**

```
public static int countOccurrences(String str, char c) {
    return StringUtils.countMatches(str, c);
}
```

**Solution 4: Using RegEx**

```
public static int countOccurrences(String str, char c) {
    return str.length() - str.replaceAll(String.valueOf(c), "").length();
}
```

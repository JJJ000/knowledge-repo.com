---
title: What is the process for capitalizing the initial letter of each word in a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.replaceAll() method with a regex expression to capitalize the first character of each word in a string.
---

**Contents**

[TOC]

1. Using for Loop 

```java
String str = "capitalize each word";
StringBuilder sb = new StringBuilder();
for (String s : str.split(" ")) {
    sb.append(Character.toUpperCase(s.charAt(0)))
      .append(s.substring(1))
      .append(" ");
}
String capitalized = sb.toString().trim();
System.out.println(capitalized);
```

2. Using Streams 

```java
String str = "capitalize each word";
String capitalized = Arrays.stream(str.split(" "))
                          .map(s -> s.substring(0, 1).toUpperCase() + s.substring(1))
                          .collect(Collectors.joining(" "));
System.out.println(capitalized);
```

3. Using Apache Commons Text 

```java
String str = "capitalize each word";
String capitalized = WordUtils.capitalizeFully(str);
System.out.println(capitalized);
```

4. Using Guava 

```java
String str = "capitalize each word";
String capitalized = CaseFormat.LOWER_CAMEL.to(CaseFormat.UPPER_CAMEL, str);
System.out.println(capitalized);
```

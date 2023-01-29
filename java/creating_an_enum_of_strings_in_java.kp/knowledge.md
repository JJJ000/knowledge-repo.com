---
title: What is the most effective method for creating an enumeration of strings?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The best way to create an enum of strings in Java is to use the enum keyword to declare an enum type with a list of strings as its constants.
---

**Contents**

[TOC]

**Option 1: Enum Class**

1. Create an enum class with the desired enum constants.

```java
public enum Color {
    RED, GREEN, BLUE
}
```

2. Use the enum constants in your code.

```java
Color color = Color.RED;
```

**Option 2: EnumSet**

1. Create a Set containing the desired enum constants.

```java
Set<Color> colors = EnumSet.of(Color.RED, Color.GREEN, Color.BLUE);
```

2. Use the Set in your code.

```java
if (colors.contains(Color.RED)) {
    // do something
}
```

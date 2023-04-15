---
title: A for-loop to loop through each element of an enum in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: For each enum constant, use a for-loop to iterate over the enum, e.g. `for (MyEnum myEnum  MyEnum.values()) { ... }`.
---

**Contents**

[TOC]

**Syntax:**
```
for (EnumType variable : EnumType.values()) {
    // code block to be executed
}
```

**Example:**
```
public enum Color {
    RED, GREEN, BLUE
}

for (Color c : Color.values()) {
    System.out.println(c);
}
```

**Output:**
```
RED
GREEN
BLUE
```

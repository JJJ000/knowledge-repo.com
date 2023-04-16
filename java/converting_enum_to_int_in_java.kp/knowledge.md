---
title: What is the process for changing an enum value to an integer?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The int value of an enum can be obtained by calling the ordinal() method on the enum.
---

**Contents**

[TOC]

# Section 1: Overview

Enums are a feature of the Java programming language that allow developers to create a list of constants. Enums are typically used to represent a set of fixed values, such as a list of days of the week, or a list of colors.

# Section 2: Converting Enum to Int

In Java, it is possible to convert an enum value to an integer. This can be done by using the ordinal() method of the enum, which returns the position of the enum value in the enum list. For example, if the enum list contains three values (RED, GREEN, BLUE), then RED would have an ordinal value of 0, GREEN would have an ordinal value of 1, and BLUE would have an ordinal value of 2.

# Section 3: Example Code

The following code snippet shows how to convert an enum value to an integer:

```
public enum Color {
    RED, GREEN, BLUE;
}

public int getColorAsInt(Color color) {
    return color.ordinal();
}
```

# Section 4: Conclusion

In summary, it is possible to convert an enum value to an integer in Java by using the ordinal() method of the enum. This can be useful when needing to represent a set of fixed values as integers.

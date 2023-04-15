---
title: Change from an ordinal number in an enumerated type to the corresponding enumerated type
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The enum type in Java can be obtained by calling the Enum.valueOf() method with the enum`s name and the ordinal as parameters.
---

**Contents**

[TOC]

### Overview 
Enums in Java are used to define a set of predefined constants. Enums can be represented by both a name and an ordinal value. This article covers how to convert from an enum ordinal to an enum type in Java.

### Using the values() Method 
The values() method of the Enum class can be used to get an array of all the enum constants. This array can then be used to get the enum type from its ordinal value. 

### Example

```java
public enum Color {
    RED, GREEN, BLUE;
}

public static Color getColorFromOrdinal(int ordinal) {
    return Color.values()[ordinal];
}
```

### Conclusion
Converting from an enum ordinal to an enum type in Java can be done using the values() method of the Enum class. This method returns an array of all the enum constants, which can then be used to get the enum type from its ordinal value.

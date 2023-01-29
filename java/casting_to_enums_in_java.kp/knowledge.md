---
title: Convert an integer to an enumerated type in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Enum values can be cast from an int by calling Enum.valueOf(enumType, intValue).
---

**Contents**

[TOC]

### What is an Enum?
Enums in Java are a special type of class that represent a group of constants. They are used to represent a fixed set of values that can be used in a program.

### How to Cast an Int to an Enum
In order to cast an int to an enum, you must first define the enum type with the values you want to use. This is done by creating a class that extends the Enum class, and then defining the constants you want to use in the enum.

Once the enum type is defined, you can cast an int to the enum by using the static valueOf() method. This method takes a String parameter and returns the corresponding enum constant.

### Example
For example, if you wanted to cast an int to an enum representing the days of the week, you could define the enum type as follows:

```java
public enum Day {
    SUNDAY,
    MONDAY,
    TUESDAY,
    WEDNESDAY,
    THURSDAY,
    FRIDAY,
    SATURDAY
}
```

You can then cast an int to the corresponding day of the week by using the valueOf() method:

```java
int dayNumber = 2;
Day day = Day.valueOf(dayNumber);
System.out.println(day); // Outputs "TUESDAY"
```

### Conclusion
Casting an int to an enum in Java is a simple process that requires defining the enum type and then using the valueOf() method to cast the int. This can be used to represent a fixed set of values in a program, making it easier to work with them.

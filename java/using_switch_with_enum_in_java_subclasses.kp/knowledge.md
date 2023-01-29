---
title: Using a switch statement with an enum inside a subclass in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, it is possible to use a switch statement with an enum under a subclass.
---

**Contents**

[TOC]

### Overview
Using a switch statement with an enum is a powerful way to create a more organized and efficient codebase. Enums are special data types that can be used to represent a set of constants, such as the days of the week or a list of possible states. When used in combination with a switch statement, the code can be more concise and easier to read.

### Syntax
The syntax for using a switch statement with an enum is similar to a regular switch statement, but with an enum instead of an integer or other data type. The syntax looks like this:

```java
switch (enumVariable) {
  case ENUM_CONSTANT_1:
    // code to be executed
    break;
  case ENUM_CONSTANT_2:
    // code to be executed
    break;
  ...
  default:
    // code to be executed
    break;
}
```

### Example
For example, if you have an enum that contains the days of the week, you can use a switch statement to execute different code for each day:

```java
enum DaysOfTheWeek {
  SUNDAY,
  MONDAY,
  TUESDAY,
  WEDNESDAY,
  THURSDAY,
  FRIDAY,
  SATURDAY
}

DaysOfTheWeek day = DaysOfTheWeek.MONDAY;

switch (day) {
  case SUNDAY:
    System.out.println("It's Sunday!");
    break;
  case MONDAY:
    System.out.println("It's Monday!");
    break;
  case TUESDAY:
    System.out.println("It's Tuesday!");
    break;
  case WEDNESDAY:
    System.out.println("It's Wednesday!");
    break;
  case THURSDAY:
    System.out.println("It's Thursday!");
    break;
  case FRIDAY:
    System.out.println("It's Friday!");
    break;
  case SATURDAY:
    System.out.println("It's Saturday!");
    break;
  default:
    System.out.println("Invalid day!");
    break;
}
```

### Subclasses
Using a switch statement with an enum can also be useful when working with subclasses. For example, if you have a base class and multiple subclasses, you can use a switch statement to execute different code depending on the type of subclass.

For example, consider the following code:

```java
class Base {
  // code
}

class SubclassA extends Base {
  // code
}

class SubclassB extends Base {
  // code
}

Base base = new SubclassA();

switch (base) {
  case SubclassA:
    // code to be executed
    break;
  case SubclassB:
    // code to be executed
    break;
  default:
    // code to be executed
    break;
}
```

In this example, the code in the switch statement will be executed depending on the type of subclass.

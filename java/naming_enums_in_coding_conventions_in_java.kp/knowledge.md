---
title: Naming enumerations in coding conventions
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Enums in Java should be named using all uppercase letters, with each word separated by an underscore.
---

**Contents**

[TOC]

### CamelCase
Enums in Java should follow the conventional CamelCase naming style. This means that the first letter of each word in the enum should be capitalized. For example:

```java
public enum CarType {
    SEDAN, SUV, HATCHBACK, CONVERTIBLE
}
```

### Consistent Naming
Enum names should be consistent and descriptive. Avoid using abbreviations, as they can be confusing and difficult to remember. For example, instead of using the abbreviation "SUV" use "SportUtilityVehicle".

### Avoid Plurals
It is generally not recommended to use plurals when naming enums in Java. For example, instead of using "CARS", use "CAR".

### Avoid Reserved Words
Avoid using Java reserved words when naming enums. For example, instead of using "public" use "PublicAccess".

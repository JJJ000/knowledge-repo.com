---
title: Is it possible to make a constructor in Java private?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, a constructor in Java can be private.
---

**Contents**

[TOC]

## Yes
A constructor can be private in Java. Private constructors are used in classes that contain only static members. A private constructor prevents other classes from instantiating the class.

## Example
For example, consider a class that only contains static methods and fields.

```java
public class UtilityClass {
    private UtilityClass() {
        // private constructor
    }

    public static void doSomething() {
        // ...
    }
}
```

In this case, the private constructor prevents other classes from instantiating the UtilityClass.

## Benefits
Using a private constructor can be beneficial in certain cases. It can be used to ensure that no other classes can instantiate the class, which can help prevent accidental misuse of the class.

## Disadvantages
The main disadvantage of using a private constructor is that it limits the flexibility of the class. It prevents other classes from extending the class, which may be necessary in certain cases.

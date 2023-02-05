---
title: What is the syntax for using null in a switch statement?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Null can be used as a valid expression in a switch statement in Java, as long as it is the only expression present.
---

**Contents**

[TOC]

## Introduction

Null is a special keyword in Java that is used to represent the absence of a value. It is often used to represent an empty value or an error condition. In Java, null can be used in switch statements as a valid value. This allows a programmer to use null as a way to provide a default case for a switch statement.

## Using Null in Switch

Using null in a switch statement is similar to using any other value. The null value is evaluated against the switch expression and then the corresponding case statement is executed. If the switch expression does not match any of the case statements, then the default case is executed.

It is important to note that the switch expression must be of a type that can be compared to the null value. This means that the switch expression must be of a reference type, such as an object or array. Primitive types, such as int or char, cannot be compared to the null value.

## Example

The following example demonstrates how to use null in a switch statement.

```
String input = null;

switch (input) {
    case "abc":
        System.out.println("Input is abc");
        break;
    case "def":
        System.out.println("Input is def");
        break;
    default:
        System.out.println("Input is null");
        break;
}
```

In this example, the switch expression is a String variable named input. The input variable is set to null, so the default case will be executed. The output of this program will be "Input is null".

## Conclusion

Null can be used in switch statements as a valid value. It is important to note that the switch expression must be of a reference type in order to be compared to the null value. This allows a programmer to use null as a way to provide a default case for a switch statement.

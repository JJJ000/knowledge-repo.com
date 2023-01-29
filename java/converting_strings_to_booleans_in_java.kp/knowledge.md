---
title: What is the process of converting a string object to a boolean object?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Boolean.valueOf() method to convert a String object to a Boolean object in Java.
---

**Contents**

[TOC]

### Using parseBoolean()
The `parseBoolean()` method of the `Boolean` class is used to convert a String object to a Boolean object. This method takes a String value as an argument and returns a Boolean object.

### Syntax
The syntax for using the `parseBoolean()` method is as follows:

`Boolean.parseBoolean(String str)`

### Example
The following code snippet shows an example of how to use the `parseBoolean()` method to convert a String object to a Boolean object:

```java
String str = "true";
Boolean bool = Boolean.parseBoolean(str);
System.out.println(bool); // Outputs true
```

### Caveats
It is important to note that the `parseBoolean()` method is case sensitive and will only return `true` if the String argument is equal to "true" (ignoring case). Any other String value will return `false`.

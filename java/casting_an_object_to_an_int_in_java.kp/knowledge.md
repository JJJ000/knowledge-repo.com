---
title: Converting an object to an int
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the intValue() method of the Integer class to cast an Object to an int in Java.
---

**Contents**

[TOC]

## Converting an Object to an int

1. Retrieve the desired data from the Object. 
2. Convert the data to a String.
3. Use the Integer.parseInt() method to convert the String to an int.

## Example Code

```java
Object obj = 5;
String str = obj.toString();
int number = Integer.parseInt(str);
```

## Further Reading

For more information on converting objects to ints, please see the [Java Documentation](https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html#parseInt(java.lang.String)).

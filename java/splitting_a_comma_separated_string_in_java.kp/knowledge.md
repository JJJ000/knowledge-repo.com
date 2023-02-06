---
title: What is the best way to divide a string that is separated by commas?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String.split() method, passing in a comma (`,`) as the delimiter.
---

**Contents**

[TOC]

# Step 1: Get the String

The first step is to get the string that needs to be split. This can be done by creating a variable and assigning it the string to be split:

```java
String str = "This,is,a,comma,separated,string";
```

# Step 2: Split the String

The next step is to split the string. This can be done by using the `split()` method of the `String` class. The `split()` method takes a regular expression as its argument, and it returns an array of strings split by the given regular expression. In this case, the regular expression is a comma (`,`):

```java
String[] splittedStr = str.split(",");
```

# Step 3: Iterate Through the Array

The third step is to iterate through the array of strings that the `split()` method returned. This can be done using a for loop:

```java
for (String s : splittedStr) {
    System.out.println(s);
}
```

# Step 4: Print the Results

The fourth and final step is to print the results. This can be done by using the `println()` method of the `System.out` class:

```java
System.out.println("This");
System.out.println("is");
System.out.println("a");
System.out.println("comma");
System.out.println("separated");
System.out.println("string");
```

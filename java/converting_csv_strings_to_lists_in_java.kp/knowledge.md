---
title: What is the process for transforming a comma-separated string into a list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using the Arrays.asList() method, a comma-separated String can be converted to a List in Java.
---

**Contents**

[TOC]

### Define a Method

The first step to convert a comma-separated String to List in Java is to define a method that takes the String as an argument and returns a List.

For example:

```
public static List<String> convertStringToList(String str) {
    // code to convert comma-separated String to List goes here
}
```

### Split the String

The next step is to split the String into individual elements using the `split()` method. This method takes a regular expression as an argument and returns an array of Strings.

For example:

```
String[] elements = str.split(",");
```

### Create a List

The third step is to create a new List object to store the individual elements. This can be done by using the `ArrayList` class.

For example:

```
List<String> list = new ArrayList<>();
```

### Add Elements to the List

The final step is to add the individual elements from the array to the List using a `for` loop.

For example:

```
for (String element : elements) {
    list.add(element);
}
```

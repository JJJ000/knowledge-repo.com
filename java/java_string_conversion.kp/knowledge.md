---
title: Turn an array of strings into a single string in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.join() method to join the elements of the array into a single string.
---

**Contents**

[TOC]

#Solution 1:

Using the `String.join()` Method
--------------------------------
The `String.join()` method can be used to join an array of strings into a single string. The syntax is as follows:

```
String.join(delimiter, array);
```

Where `delimiter` is the string used to separate each element of the array, and `array` is the array of strings to be joined.

For example:

```
String[] array = {"Hello", "World"};
String joinedString = String.join(" ", array);
// joinedString = "Hello World"
```

#Solution 2:

Using a `for` Loop
------------------
A `for` loop can be used to iterate through an array of strings, concatenating each element to a single string. The syntax is as follows:

```
String joinedString = "";
for (String s : array) {
    joinedString += s;
}
```

Where `array` is the array of strings to be joined and `joinedString` is the string to contain the joined elements.

For example:

```
String[] array = {"Hello", "World"};
String joinedString = "";
for (String s : array) {
    joinedString += s;
}
// joinedString = "HelloWorld"
```

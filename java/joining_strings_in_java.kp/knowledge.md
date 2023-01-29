---
title: Create a string from a list of strings using the Java join() method
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String join() method to join the elements of the List into a String, separated by the desired delimiter.
---

**Contents**

[TOC]

### Preparation

Before joining the list of strings, it is important to prepare the list. This can be done by ensuring that all entries are valid strings and that there are no null values in the list.

### Joining the Strings

Once the list is prepared, the strings can be joined together. This is done using the `join()` method, which takes two parameters: a delimiter and the list of strings to join. For example, to join the list of strings with a comma delimiter:

```java
String joinedString = String.join(",", listOfStrings);
```

### Customization

The `join()` method can be customized to suit the needs of the application. For example, the delimiter can be changed to any character or string, and there are various options for handling null values.

### Output

The result of the `join()` method is a single string containing all of the elements of the list, separated by the delimiter. This string can then be used as necessary in the application.

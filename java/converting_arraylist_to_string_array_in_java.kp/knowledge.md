---
title: Change an arraylist of strings into a string array
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the toArray() method of the ArrayList class to convert an ArrayList<String> to a String[] array.
---

**Contents**

[TOC]

### Overview

The conversion of an ArrayList of Strings to a String array in Java is a relatively straightforward process. The ArrayList class provides a toArray() method which can be used to convert the ArrayList into an array of the specified type. In this case, the specified type is a String array. 

### Syntax

The syntax for the toArray() method is as follows:

```java
String[] array = list.toArray(new String[list.size()]);
```

where `list` is the ArrayList of Strings.

### Example

The following is an example of how to convert an ArrayList of Strings to a String array in Java:

```java
ArrayList<String> list = new ArrayList<>();
list.add("Hello");
list.add("World");

String[] array = list.toArray(new String[list.size()]);
```

### Output

The output of the above code is an array of Strings with the following values:

```
[Hello, World]
```

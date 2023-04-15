---
title: A fast and simple method for combining array elements with a delimiter (the opposite of split) in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.join() method to join array elements with a separator.
---

**Contents**

[TOC]

**Using String.join()**

String.join() is a static method of the String class that allows you to join array elements with a separator.

**Syntax**

String.join(separator, array);

**Example**

String[] array = {"Hello", "World"};
String joinedString = String.join(",", array);
// Output: "Hello,World"

**Using StringBuilder**

StringBuilder is a mutable sequence of characters that allows you to join array elements with a separator.

**Syntax**

StringBuilder sb = new StringBuilder();
for (int i = 0; i < array.length; i++) {
    sb.append(array[i]);
    if (i < array.length - 1) {
        sb.append(separator);
    }
}
String joinedString = sb.toString();

**Example**

String[] array = {"Hello", "World"};
StringBuilder sb = new StringBuilder();
for (int i = 0; i < array.length; i++) {
    sb.append(array[i]);
    if (i < array.length - 1) {
        sb.append(",");
    }
}
String joinedString = sb.toString();
// Output: "Hello,World"

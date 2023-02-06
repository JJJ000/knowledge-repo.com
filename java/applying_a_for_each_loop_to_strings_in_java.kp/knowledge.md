---
title: What is the syntax for using a for-each loop to iterate through every character in a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To apply a for-each loop to every character in a String in Java, use a for-each loop to iterate through the characters of the String.
---

**Contents**

[TOC]

1. Preparing the String

First, you must create a `String` object containing the desired characters. This can be done by either declaring a `String` variable and assigning it a value, or by calling the `String` class constructor with the desired characters as the argument.

2. Creating a `char[]` Array

Next, you must create a `char[]` array containing the characters of the `String` object. This can be done by calling the `toCharArray()` method on the `String` object, which will return a `char[]` array containing the characters of the `String`.

3. Iterating Through the `char[]` Array

After creating the `char[]` array, you can use a for-each loop to iterate through it. The syntax for this is as follows:

```
for (char c : charArray) {
    // do something with c
}
```

4. Doing Something With Each Character

Finally, you can use the `char` variable `c` within the loop body to do something with each character in the `String`. This could be anything from printing it out to the console, to performing calculations on it.

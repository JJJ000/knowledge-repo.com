---
title: Converting a Java integer to a string - the difference between using integer.tostring(i) and new integer(i).tostring()
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Integer.toString(i) is the preferred method for converting an int to a String.
---

**Contents**

[TOC]

### Integer.toString(i)

This method is a static method of the Integer class. It takes an int value as an argument and returns the String representation of it. It is the simplest and most efficient way to convert an int value to a String.

### new Integer(i).toString()

This method creates an Integer object from the given int value and then calls the toString() method on the object. It is not as efficient as the Integer.toString(i) method, since it requires the creation of an object.

### Advantages of Integer.toString(i)

- It is more efficient than the new Integer(i).toString() method.
- It is simpler to use and understand.

### Disadvantages of Integer.toString(i)

- It does not allow for any customization of the output String.

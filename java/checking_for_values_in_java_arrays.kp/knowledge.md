---
title: What is the process for checking if a Java array contains a specific value?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Use the `Arrays.asList(array).contains(value)` method to determine if an array contains a particular value in Java.
---

**Contents**

[TOC]

### Option 1: Using Stream API

1. Create a Stream of the array using `Arrays.stream()`
2. Use `anyMatch()` to check if the value exists in the array

### Option 2: Using for-each loop

1. Create a for-each loop to iterate through the array
2. Use `equals()` to compare the value with each element in the array

### Option 3: Using for loop

1. Create a for loop to iterate through the array
2. Use `equals()` to compare the value with each element in the array

### Option 4: Using contains()

1. Use `Arrays.asList()` to convert the array to a List
2. Use `contains()` to check if the value exists in the List

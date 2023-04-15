---
title: What is the process for changing an arraylist of integers into a primitive int array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `toArray()` method to convert the ArrayList to a primitive int array.
---

**Contents**

[TOC]

### Create a Primitive Array

The first step to converting an ArrayList containing Integers to a primitive int array is to create an int array with the same size as the ArrayList. This can be done using the `size()` method of the ArrayList, which returns the number of elements in the list.

### Populate the Primitive Array

Once the int array has been created, it must be populated with the values from the ArrayList. This can be done using a for loop, which will iterate through the ArrayList and add each value to the int array.

### Convert ArrayList to Primitive Array

The final step is to convert the ArrayList to a primitive int array. This can be done using the `toArray()` method of the ArrayList, which takes an int array as an argument and returns an array containing the elements of the ArrayList.

### Use the Primitive Array

Once the ArrayList has been successfully converted to a primitive int array, it can be used just like any other int array. This includes looping through the array, accessing individual elements, and passing the array to other methods.

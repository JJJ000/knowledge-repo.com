---
title: What is the process for making a general array in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A generic array can be created using the syntax `Type[] arrayName = new Type[size];`.
---

**Contents**

[TOC]

### Declaring the Array

To create a generic array, you must first declare the array. To do this, you must specify the type of the array, followed by the array's name and the size of the array in square brackets. For example:

`Integer[] myArray = new Integer[10];`

This declares an array of 10 Integer objects, called myArray.

### Initializing the Array

Once the array is declared, you can initialize the array with values. This can be done by assigning values to each index of the array. For example:

`myArray[0] = 5;`

This assigns the value 5 to the first index of the array.

### Accessing the Array

Once the array is initialized, you can access the values stored in the array. This can be done by using the array's name and the index of the array. For example:

`int value = myArray[0];`

This assigns the value stored in the first index of the array to the variable value.

### Iterating Through the Array

You can also iterate through the array to access all of the values stored in the array. This can be done using a for loop. For example:

`for (int i = 0; i < myArray.length; i++) {
    int value = myArray[i];
    System.out.println(value);
}`

This loop iterates through the entire array, printing out the value stored in each index.

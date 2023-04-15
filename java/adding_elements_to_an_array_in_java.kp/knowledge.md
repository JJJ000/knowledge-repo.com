---
title: What is the process for inserting new items into an array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can add new elements to an array in Java by using the ArrayList class or the Arrays.copyOf() method.
---

**Contents**

[TOC]

### Creating the Array

In Java, an array is an object that holds a fixed number of values of a single type. The syntax for creating an array is:

`datatype[] arrayName = new datatype[size];`

Where `datatype` is the type of data the array will hold, `arrayName` is the name of the array, and `size` is the number of elements the array will hold.

### Adding Elements

Once the array is created, elements can be added to it using the array's index. The syntax for adding an element to an array is:

`arrayName[index] = element;`

Where `index` is the position in the array where the element should be inserted and `element` is the value to be inserted.

### Updating the Array Size

When adding elements to an array, it is important to remember to update the array's size. This can be done by creating a new array with a larger size and copying the elements from the old array to the new array. The syntax for creating a new array and copying the elements is:

`datatype[] newArrayName = new datatype[newSize];`

`System.arraycopy(arrayName, 0, newArrayName, 0, arrayName.length);`

Where `newSize` is the size of the new array and `arrayName` is the name of the old array.

### Adding the Element

Once the new array is created, the element can be added at the desired index. The syntax for adding an element to an array is:

`newArrayName[index] = element;`

Where `index` is the position in the array where the element should be inserted and `element` is the value to be inserted.

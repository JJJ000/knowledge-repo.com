---
title: What is the correct syntax for creating a string array in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: String[] can be initialized using the syntax `String[] arrayName = new String[arraySize];`.
---

**Contents**

[TOC]

1. #### Creating an Empty String Array
   To create an empty String array in Java, you can use the following syntax:
   ```
   String[] arrayName = new String[size];
   ```
   Here, `size` is the number of elements that the array will hold.

2. #### Initializing a String Array with Values
   To initialize a String array with values, you can use the following syntax:
   ```
   String[] arrayName = new String[]{"value1", "value2", "value3"};
   ```
   Here, `value1`, `value2`, and `value3` are the initial values of the array.

3. #### Initializing a String Array with a Fixed Size and Values
   To initialize a String array with a fixed size and values, you can use the following syntax:
   ```
   String[] arrayName = new String[size]{"value1", "value2", "value3"};
   ```
   Here, `size` is the number of elements that the array will hold, and `value1`, `value2`, and `value3` are the initial values of the array.

4. #### Initializing a String Array with an Array of Strings
   To initialize a String array with an array of Strings, you can use the following syntax:
   ```
   String[] arrayName = new String[]{stringArray};
   ```
   Here, `stringArray` is the array of Strings that will be used to initialize the array.

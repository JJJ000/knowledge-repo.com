---
title: What is the process for determining how many times an element appears in a list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the Collections.frequency() method to count the number of occurrences of an element in a List in Java.
---

**Contents**

[TOC]

**Section 1: Using a for loop** 

1. Create a variable to hold the count of the element in the list and initialize it to 0. 
2. Use a for loop to iterate over the list.
3. For each element in the list, check if it is equal to the element whose count we are trying to find. 
4. If it is, increment the count variable by 1.
5. After the loop is finished, the count variable will contain the number of occurrences of the element in the list.

**Section 2: Using a while loop**

1. Create a variable to hold the count of the element in the list and initialize it to 0.
2. Create a variable to hold the index of the current element in the list and initialize it to 0.
3. Use a while loop to iterate over the list.
4. For each element in the list, check if it is equal to the element whose count we are trying to find. 
5. If it is, increment the count variable by 1.
6. Increment the index variable by 1.
7. After the loop is finished, the count variable will contain the number of occurrences of the element in the list.

**Section 3: Using a for-each loop**

1. Create a variable to hold the count of the element in the list and initialize it to 0.
2. Use a for-each loop to iterate over the list.
3. For each element in the list, check if it is equal to the element whose count we are trying to find. 
4. If it is, increment the count variable by 1.
5. After the loop is finished, the count variable will contain the number of occurrences of the element in the list.

**Section 4: Using the Java Streams API**

1. Use the Java Streams API to create a Stream from the list.
2. Use the Stream's filter() method to filter the stream for elements that are equal to the element whose count we are trying to find.
3. Use the Stream's count() method to count the number of elements that match the filter.
4. The count() method will return the number of occurrences of the element in the list.

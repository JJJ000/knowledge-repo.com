---
title: What is the process for reversing an int array in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To reverse an int array in Java, use the ArrayUtils.reverse() method from the Apache Commons Lang library.
---

**Contents**

[TOC]

## Solution 1: Using a For Loop

1. Initialize an empty array of the same size as the input array. 
2. Create a loop that starts at the last index of the input array and decrements the index by 1. 
3. Inside the loop, assign the element of the input array at the current index to the corresponding index in the empty array. 
4. Return the reversed array. 

## Solution 2: Using the Java 8 Stream API

1. Create a Stream from the input array. 
2. Use the `collect()` method with a `Collectors.toList()` collector to convert the Stream into a List.
3. Use the `Collections.reverse()` method to reverse the order of elements in the List.
4. Use the `toArray()` method to convert the List back into an array and return it.

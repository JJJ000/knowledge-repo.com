---
title: Mixing up the order of elements in an array
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Collections.shuffle() can be used to randomly shuffle an array in Java.
---

**Contents**

[TOC]

# Solution 1:

Using Collections.shuffle()

1. Create an array of elements
2. Create a List from the array
3. Use Collections.shuffle() to shuffle the elements in the list
4. Convert the List back to an array

# Solution 2:

Using Random class

1. Create an array of elements
2. Create a Random object
3. Iterate over the array and swap each element with a random element in the array
4. Repeat the process until all elements are shuffled

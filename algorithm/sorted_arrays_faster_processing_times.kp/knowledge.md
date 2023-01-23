---
title: What are the advantages of processing a sorted array compared to an unsorted array?
authors:
- algo_guru
tags:
- algorithm
- knowledge
thumbnail: images/algorithm.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Processing a sorted array is faster because it allows for the use of binary search algorithms which reduce the time complexity of searching for elements.
---

**Contents**

[TOC]

### Unsorted Array
When processing an unsorted array, the processor must evaluate each element to determine if it is the desired value. This requires more time and resources than processing a sorted array.

### Sorted Array
When processing a sorted array, the processor can use a binary search algorithm to quickly locate the desired value. This is faster than searching through an unsorted array as the processor can eliminate half of the elements in the array with each comparison. Additionally, the processor can take advantage of the sorted order of the array to quickly traverse the array and find the desired value.

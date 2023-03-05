---
title: What is the implementation of python's list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Python`s list is implemented using an array-based data structure that allows for dynamic resizing and indexing of elements.
---

**Contents**

[TOC]

## Dynamic Arrays

Python's `list` is implemented as a dynamic array that can grow or shrink in size dynamically. A dynamic array is an abstract data type that allows for insertion, deletion, and random access of elements, and its size can be changed during runtime. In a dynamic array, elements of an array are stored in adjacent memory locations, and the size of the array is determined at runtime based on its need. This means that when a new element is added to a dynamic array, the array's size is increased, and when an element is deleted, the array's size is decreased.

## Allocation of Memory

Whenever a new list is created in Python, a block of memory is allocated to store its elements. Initially, the size of this block of memory is determined based on the number of elements that are expected to be stored in the list. However, if more elements are added to the list than initially anticipated, the memory block is reallocated to a larger block of memory. Similarly, if elements are removed from the list, the memory block may be resized to a smaller block of memory to conserve memory.

## Operations on List

Python's list implements various operations such as index, append, insert, remove, and pop operations in constant or amortized constant time complexity. The index operation takes constant time since the list's elements are stored in contiguous memory locations, and the computer can quickly calculate the memory address of an element based on its index. Similarly, the append operation also takes constant time, as it only requires the allocation of additional memory for the new element.

## Limitations

Although a dynamic array is a highly efficient data structure for storing and accessing elements, it has a few limitations. Firstly, dynamic arrays consume memory proportional to the number of elements stored in them, even if some of the elements are empty. Secondly, when a dynamic array is resized, it may require copying all elements from the old memory block to the new memory block, which can be expensive for large arrays. Finally, dynamic arrays are not suitable for inserting or deleting elements in the middle of the array, as it requires shifting all the subsequent elements by one position, resulting in a linear time complexity.

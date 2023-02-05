---
title: A quick method to rearrange the order of items in a list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The most efficient way to rotate a list in Python is to use the deque.rotate() function from the collections module.
---

**Contents**

[TOC]

**Solution 1: Using the slicing technique**

This approach is the most efficient way to rotate a list in Python. It involves slicing the list in two parts and then reversing the order of the elements.

1. Split the list into two parts:
   - The first part consists of the elements from the start of the list up to the element at the rotation point. 
   - The second part consists of the elements from the rotation point to the end of the list.
2. Reverse the order of the elements in each part:
   - Reverse the order of the elements in the first part. 
   - Reverse the order of the elements in the second part.
3. Join the two parts:
   - Join the first part and the second part together in the desired order.

**Solution 2: Using the deque class**

This approach is also efficient and involves using the deque class from the collections module. 

1. Create a deque object from the list:
   - Create a deque object from the list using the deque() constructor. 
2. Rotate the deque object:
   - Rotate the deque object by the desired number of elements using the rotate() method.
3. Convert the deque object to a list:
   - Convert the deque object back to a list using the list() constructor. 

**Solution 3: Using the list.insert() method**

This approach is also efficient and involves using the list.insert() method.

1. Get the element at the rotation point:
   - Get the element at the rotation point using list indexing. 
2. Insert the element at the start of the list:
   - Insert the element at the start of the list using the list.insert() method. 
3. Remove the element from its original position:
   - Remove the element from its original position using the list.remove() method. 

**Solution 4: Using the list.append() method**

This approach is also efficient and involves using the list.append() method.

1. Get the element at the rotation point:
   - Get the element at the rotation point using list indexing. 
2. Append the element to the end of the list:
   - Append the element to the end of the list using the list.append() method. 
3. Remove the element from its original position:
   - Remove the element from its original position using the list.remove() method.

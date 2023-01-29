---
title: Eliminating duplicate entries in lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To remove duplicates from a list in Python, use the set() function.
---

**Contents**

[TOC]

**Section 1: Using Sets**

Sets are a powerful data structure in Python that can be used to remove duplicates from a list. A set is an unordered collection of unique elements, meaning that no duplicate elements can exist within a set. To remove duplicates from a list, convert the list into a set, then convert the set back into a list.

```python
# Create a list with duplicate elements 
myList = [1, 2, 3, 4, 4, 5, 6, 6, 7, 8]

# Convert the list into a set 
mySet = set(myList)

# Convert the set back into a list 
myNewList = list(mySet)

print(myNewList) 
# Output: [1, 2, 3, 4, 5, 6, 7, 8]
```

**Section 2: Using a For Loop**

Another way to remove duplicates from a list is to use a for loop. In this approach, a new list is created and each element from the original list is checked against the new list. If the element is not already present in the new list, it is added to the new list.

```python
# Create a list with duplicate elements 
myList = [1, 2, 3, 4, 4, 5, 6, 6, 7, 8]

# Create a new list
myNewList = []

# Loop through the original list and add each element to the new list 
# if it's not already present
for i in myList:
    if i not in myNewList:
        myNewList.append(i)

print(myNewList) 
# Output: [1, 2, 3, 4, 5, 6, 7, 8]
```

**Section 3: Using List Comprehension**

List comprehension is a powerful tool in Python that can be used to create a new list from an existing list. To remove duplicates from a list, a new list is created that contains only the elements from the original list that are not already present in the new list.

```python
# Create a list with duplicate elements 
myList = [1, 2, 3, 4, 4, 5, 6, 6, 7, 8]

# Create a new list with only the elements that are not already present 
myNewList = [i for i in myList if i not in myNewList]

print(myNewList) 
# Output: [1, 2, 3, 4, 5, 6, 7, 8]
```

**Section 4: Using the Built-in Function**

Python also provides a built-in function called `set()` that can be used to remove duplicates from a list. The `set()` function will take a list as an argument and return a new set without any duplicate elements. The set can then be converted back into a list.

```python
# Create a list with duplicate elements 
myList = [1, 2, 3, 4, 4, 5, 6, 6, 7, 8]

# Remove duplicates from the list 
myNewList = list(set(myList))

print(myNewList) 
# Output: [1, 2, 3, 4, 5, 6, 7, 8]
```

---
title: Converting a Python set to a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To convert a Python set to a list, use the list() function.
---

**Contents**

[TOC]

## Converting a Set to List using list() Method

The python built-in method `list()` can be used to convert a set to list. We can simply pass the set to `list()` method and it'll return a list containing all the elements of the set in the order they are inserted. Here is an example:

```python
# Creating a set
mySet = {1, 2, 3, 4, 5}
  
# Converting set to list
myList = list(mySet)
  
# Printing the list
print(myList)
```

Output:
```
[1, 2, 3, 4, 5]
```



## Converting a Set to List using Loop

In python, we can also convert a set to list using loops. We can create an empty list and then loop through each element of the set and append it to the list. Here is an example:

```python
# Creating a set
mySet = {1, 2, 3, 4, 5}
  
# Creating an empty list
myList = []
  
# Looping through each element of set and appending to myList
for x in mySet:
    myList.append(x)
  
# Printing the list
print(myList)
```

Output:
```
[1, 2, 3, 4, 5]
```



## Converting a Set to List using Set Comprehension

Python set comprehension provides a concise way to create a new set by reusing elements from an existing set. It can also be used to convert a set to a list. Here is an example:

```python
# Creating a set
mySet = {1, 2, 3, 4, 5}
  
# Converting set to list using set comprehension
myList = [x for x in mySet]
  
# Printing the list
print(myList)
```

Output:
```
[1, 2, 3, 4, 5]
```

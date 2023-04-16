---
title: Adding the elements of two lists together element by element
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The element-wise addition of two lists in Python can be done using the zip() function and list comprehension.
---

**Contents**

[TOC]

### Method 1: Using zip()

Using the zip() function, we can add two lists element-wise by zipping them together and then using a list comprehension to add them up.

```python
list1 = [1, 2, 3] 
list2 = [4, 5, 6] 
  
# using zip() to add lists 
# and convert to set 
result = [sum(i) for i in zip(list1, list2)] 
  
# printing result  
print("Element-wise sum of list is : " + str(result)) 
```

### Method 2: Using numpy.add()

Using the numpy.add() function, we can add two lists element-wise by converting them to numpy arrays and then using the numpy.add() function to add them up.

```python
import numpy as np 
  
list1 = [1, 2, 3] 
list2 = [4, 5, 6] 
  
# using numpy.add() to add lists 
result = np.add(list1, list2) 
  
# printing result  
print("Element-wise sum of list is : " + str(result)) 
```

### Method 3: Using map()

Using the map() function, we can add two lists element-wise by mapping a lambda function to them and then converting the map object to a list.

```python
list1 = [1, 2, 3] 
list2 = [4, 5, 6] 
  
# using map() to add lists 
result = list(map(lambda x, y: x + y, list1, list2)) 
  
# printing result  
print("Element-wise sum of list is : " + str(result)) 
```

### Method 4: Using for loop

Using a for loop, we can add two lists element-wise by iterating over them and adding up the elements at the same indices.

```python
list1 = [1, 2, 3] 
list2 = [4, 5, 6] 
  
# using for loop to add lists 
result = [] 
  
# Add corresponding elements 
for i in range(len(list1)): 
    result.append(list1[i] + list2[i]) 
  
# printing result  
print("Element-wise sum of list is : " + str(result)) 
```

---
title: Find the unique elements between two lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The difference between two lists with unique entries can be found by using the set.difference() method.
---

**Contents**

[TOC]

### Section 1: Using Sets
Python provides a data structure called set which is a collection of unique elements. We can use the set data structure to find the difference between two lists. 

The `difference()` method returns a set that contains the difference between two or more sets. 

Syntax:
`set1.difference(set2)`

Example:

```
list1 = [1, 2, 3, 4, 5] 
list2 = [4, 5, 6, 7, 8] 
  
# Converting lists to sets 
set1 = set(list1) 
set2 = set(list2) 
  
# Finding difference between sets 
diff_set = set1.difference(set2) 
  
# Print difference 
print(diff_set) 
```

Output:
`{1, 2, 3}`

### Section 2: Using List Comprehension
List comprehension is a powerful way to perform a task on a list. We can use list comprehension to find the difference between two lists.

Syntax:
`[element for element in list1 if element not in list2]`

Example:

```
list1 = [1, 2, 3, 4, 5] 
list2 = [4, 5, 6, 7, 8] 
  
# Using list comprehension 
diff_list = [element for element in list1 if element not in list2] 
  
# Print difference 
print(diff_list) 
```

Output:
`[1, 2, 3]`

### Section 3: Using For Loop
We can use a for loop to iterate over the elements of a list and then append the elements to a new list if they are not present in the other list.

Syntax:

```
# Initializing empty list 
diff_list = [] 
  
# Iterating over list1 
for element in list1: 
    # Checking if element is not in list2 
    if element not in list2: 
        # Appending element to diff_list 
        diff_list.append(element) 
```

Example:

```
list1 = [1, 2, 3, 4, 5] 
list2 = [4, 5, 6, 7, 8] 
  
# Initializing empty list 
diff_list = [] 
  
# Iterating over list1 
for element in list1: 
    # Checking if element is not in list2 
    if element not in list2: 
        # Appending element to diff_list 
        diff_list.append(element) 
  
# Print difference 
print(diff_list) 
```

Output:
`[1, 2, 3]`

### Section 4: Using Lambda Function
We can use lambda function to find the difference between two lists.

Syntax:
`list(filter(lambda x: x not in list2, list1))`

Example:

```
list1 = [1, 2, 3, 4, 5] 
list2 = [4, 5, 6, 7, 8] 
  
# Using lambda function 
diff_list = list(filter(lambda x: x not in list2, list1)) 
  
# Print difference 
print(diff_list) 
```

Output:
`[1, 2, 3]`

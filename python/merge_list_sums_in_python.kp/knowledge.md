---
title: Create a new list by summing the values of two existing lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a list comprehension to add the corresponding elements of the two lists and store the sums in a new list.
---

**Contents**

[TOC]

### Step 1: Create two lists 

The first step is to create two lists that we want to add together. For example, let's create two lists of integers.

``` python
list1 = [1, 2, 3, 4, 5]
list2 = [6, 7, 8, 9, 10]
```

### Step 2: Use List Comprehension to Add Elements

The next step is to add the elements of the two lists together. We can use list comprehension to achieve this. 

``` python
sum_list = [list1[i] + list2[i] for i in range(len(list1))]
```
We use the range function to loop over the lists and add the corresponding elements of list1 and list2 together. The resulting sum is then appended to the sum_list.

### Step 3: Print the Result

Finally, let's print the resulting sum_list to verify that the values have been added correctly.

``` python
print(sum_list)
```

This should output

``` python
[7, 9, 11, 13, 15]
```

### Full Code

``` python
list1 = [1, 2, 3, 4, 5]
list2 = [6, 7, 8, 9, 10]
sum_list = [list1[i] + list2[i] for i in range(len(list1))]
print(sum_list)
```

This outputs

``` python
[7, 9, 11, 13, 15]
```

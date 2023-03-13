---
title: How to eliminate all the values in a list from another list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use a list comprehension with the condition that the value is not in the first list.
---

**Contents**

[TOC]

# Introduction
In Python, we can remove all the values existing in one list from another. We use a combination of loops and conditions to achieve this. There are several ways to do this task, but we will explore the two most commonly used methods.

# Using a for loop and a conditional statement
One way to remove all values within one list from another is to use a for loop and a conditional statement. Here are the steps:

1. Set up two lists - List A and List B.
2. Iterate through each element in List A using a for loop.
3. Check if the element exists in List B using an if statement.
4. If the element exists in List B, remove it using the remove() method.
5. Repeat steps 3-4 for every element in List A.
6. Print the updated List A.

Here is the code implementation:

```
list_A = [1, 2, 3, 4, 5]
list_B = [2, 4, 6]

for i in list_A:
    if i in list_B:
        list_A.remove(i)

print(list_A)
```

The output will be: `[1, 3, 5]`

# Using a list comprehension
Another way to remove all values within one list from another is to use a list comprehension. Here are the steps:

1. Set up two lists - List A and List B.
2. Create a new list using a list comprehension that only includes elements from List A that do not exist in List B.
3. Print the new list.

Here is the code implementation:

```
list_A = [1, 2, 3, 4, 5]
list_B = [2, 4, 6]

list_C = [i for i in list_A if i not in list_B]

print(list_C)
```

The output will be: `[1, 3, 5]`

# Conclusion
The two methods outlined above are both effective ways to remove all values within one list from another in Python. However, the best method to use may vary depending on the specific requirements of your project.

---
title: What is the method for confirming whether one list is a subset of another?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the set() method to convert the lists to sets and then use the subset operator `<=` to check if one set is a subset of the other.
---

**Contents**

[TOC]

Section 1: Understanding subsets

Before we can verify if one list is a subset of another in Python, we first need to understand what is meant by a subset. In mathematics, a set A is said to be a subset of set B if and only if every element of A is also an element of B. For example, suppose we have two sets: A = {1, 2, 3} and B = {1, 2, 3, 4, 5}. In this case, we can say that A is a subset of B because every element in set A (1, 2, and 3) is also an element in set B. 

Section 2: Using sets to verify subsets

In Python, one way to check if one list is a subset of another is by converting both lists to sets and using the subset() method. The subset() method returns True if all elements in one set are also present in another set. Here's an example:

```
list1 = [1, 2, 3]
list2 = [1, 2, 3, 4, 5]
set1 = set(list1)
set2 = set(list2)
if set1.issubset(set2):
    print("List1 is a subset of List2")
else:
    print("List1 is not a subset of List2")
```

In this example, we first convert both lists to sets using the set() function. We then use the issubset() method to check if set1 is a subset of set2. If it is, we print a message saying that List1 is a subset of List2. If not, we print a message saying the opposite.

Section 3: Using all() and in to verify subsets

Another way to check if one list is a subset of another in Python is by using the all() function and the in keyword. Here's an example:

```
list1 = [1, 2, 3]
list2 = [1, 2, 3, 4, 5]
if all(elem in list1 for elem in list2):
    print("List1 is a subset of List2")
else:
    print("List1 is not a subset of List2")
```

In this example, we use a for loop to iterate over every element in list2. For each element, we check if it is present in list1 using the in keyword. If all elements in list2 are also present in list1, the all() function returns True, and we print a message saying that List1 is a subset of List2. If not, we print a message saying the opposite.

Section 4: Conclusion

In this tutorial, we've discussed how to use sets and the subset() method, as well as the all() function and the in keyword, to verify if one list is a subset of another in Python. Which method you choose will depend on your specific use case and personal preference.

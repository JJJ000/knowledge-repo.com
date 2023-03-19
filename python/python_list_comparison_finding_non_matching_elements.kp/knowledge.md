---
title: Identify the elements present in one list using Python code that are absent in the other
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To find elements in one list that are not in the other, use list comprehension and the not in operator to compare the two lists.
---

**Contents**

[TOC]

1. Introduction

When dealing with lists in Python, it is common to have to compare two different lists to find elements that are present in one list but not in the other. This task can be accomplished in a few different ways, depending on the size and type of the lists being compared. In this article, we will explore some of the most commonly used techniques for finding elements in one list that are not in the other.

2. Using set difference

One of the most straightforward ways to compare two lists and find the elements that are only present in one of them is to use the set difference method. This method works by first converting each list to a set object, and then taking the difference between them. The resulting set will contain only the elements that are present in one of the original lists, but not both. Here is an example:

```
list1 = [1, 2, 3, 4]
list2 = [2, 3, 5, 6]
set1 = set(list1)
set2 = set(list2)
difference = set1.difference(set2)
print(difference)
```

Output:
```
{1, 4}
```

In this example, we first convert list1 and list2 to set objects using the set() function. We then take the difference between set1 and set2 using the .difference() method, and store the result in a new variable called difference. Finally, we print out the contents of difference, which is a set object containing the elements 1 and 4.

3. Using list comprehension

Another common technique for finding elements in one list that are not in the other is to use a list comprehension. This method works by iterating over one list, and checking if each element is present in the other list. If the element is not present, it is added to a new list. Here is an example:

```
list1 = [1, 2, 3, 4]
list2 = [2, 3, 5, 6]
difference = [i for i in list1 if i not in list2]
print(difference)
```

Output:
```
[1, 4]
```

In this example, we iterate over list1 using a list comprehension, and check if each element is in list2. If the element is not in list2, it is added to a new list called difference. Finally, we print out the contents of difference, which is a list containing the elements 1 and 4.

4. Using set intersection

Finally, it is also possible to use the set intersection method to find elements that are present in one list but not the other. This method works similarly to the set difference method, but instead of taking the difference, we take the intersection between the two sets. The resulting set will contain only the elements that are present in both lists. We can then subtract this set from the original lists to obtain the elements that are only present in one list. Here is an example:

```
list1 = [1, 2, 3, 4]
list2 = [2, 3, 5, 6]
set1 = set(list1)
set2 = set(list2)
intersection = set1.intersection(set2)
difference = set1 - intersection
print(difference)
```

Output:
```
{1, 4}
```

In this example, we first convert list1 and list2 to set objects using the set() function. We then take the intersection between set1 and set2 using the .intersection() method, and store the result in a new variable called intersection. We then take the difference between set1 and intersection using the "-" operator, and store the result in a new variable called difference. Finally, we print out the contents of difference, which is a set object containing the elements 1 and 4.

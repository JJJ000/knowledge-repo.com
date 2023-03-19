---
title: What is the method for calculating the occurrence rate of the items in a disordered list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the Counter function from the collections module in Python to count the frequency of elements in an unordered list.
---

**Contents**

[TOC]

Section 1: Understanding the problem

Before we begin coding the solution, let's first understand the problem. We are given an unordered list of elements and we need to count the frequency of each element in the list. Let's say we have a list like this:

```
my_list = ['apple', 'banana', 'orange', 'banana', 'apple', 'apple']
```

We need to count how many times each element appears in the list. In this case, 'apple' appears 3 times, 'banana' appears 2 times, and 'orange' appears 1 time.

Section 2: Using a dictionary to count frequency

One way to solve this problem is by using a dictionary. We can iterate through the list and add each element as a key in the dictionary. If the key already exists in the dictionary, we increment the value (which represents the frequency) by 1. Here's the code:

```
my_list = ['apple', 'banana', 'orange', 'banana', 'apple', 'apple']

frequency = {}
for item in my_list:
    if item in frequency:
        frequency[item] += 1
    else:
        frequency[item] = 1

print(frequency)
```

Output:

```
{'apple': 3, 'banana': 2, 'orange': 1}
```

Section 3: Using the Counter class

Python provides a built-in class called Counter that makes it very easy to count the elements in a list. Here's how we can use it:

```
from collections import Counter

my_list = ['apple', 'banana', 'orange', 'banana', 'apple', 'apple']

counter = Counter(my_list)
print(counter)
```

Output:

```
Counter({'apple': 3, 'banana': 2, 'orange': 1})
```

Section 4: Conclusion

In this tutorial, we learned how to count the frequency of elements in an unordered list in Python. We explored two ways to do this - using a dictionary and using the Counter class. The Counter class is a very useful tool when working with lists in Python, and we should keep it in mind for future projects.

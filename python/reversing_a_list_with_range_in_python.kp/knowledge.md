---
title: Print a list in descending order using range()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Print(list(range(10, 0, -1))).
---

**Contents**

[TOC]

**Section 1 - Defining the List**

The list can be defined as follows:

```
my_list = [1, 2, 3, 4, 5]
```

**Section 2 - Using range()**

We can use the range() function to iterate through the list in reverse order. The range() function takes three parameters - start, stop, and step. The start parameter is the starting index of the list, the stop parameter is the ending index of the list, and the step parameter is the increment between each index. 

For our list, we want to start at the index of the last element (5), and decrement by one until we reach the index of the first element (1). Therefore, the parameters for the range() function will be:

```
start = 5
stop = 0
step = -1
```

**Section 3 - Printing the List in Reverse Order**

We can now use the range() function to iterate through the list in reverse order and print each element.

```
for i in range(5, 0, -1):
  print(my_list[i])
```

**Section 4 - Output**

The output of the code above will be:

```
5
4
3
2
1
```

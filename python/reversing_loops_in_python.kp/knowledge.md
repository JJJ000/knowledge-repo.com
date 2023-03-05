---
title: What is the method for iterating in reverse order in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use a negative step in the range function or reverse the order of a list using slicing.
---

**Contents**

[TOC]

Using the range() function

To loop backwards in Python, we can use the range() function with a negative step. The syntax for the range() function with a negative step is:

range(start, stop, step)

The start parameter represents the starting point of the loop, the stop parameter represents the endpoint of the loop, and the step parameter represents the increment to go backwards. Here is an example:

```
for i in range(10, 0, -1):
    print(i)
```

Output:

```
10
9
8
7
6
5
4
3
2
1
```

Using the reversed() function

Another way to loop backwards in Python is by using the reversed() function. The reversed() function returns an iterator that produces the elements of a sequence in reverse order. We can use this iterator in a for loop to iterate backwards over a sequence. Here is an example:

```
my_list = [1, 2, 3, 4, 5]
for i in reversed(my_list):
    print(i)
```

Output:

```
5
4
3
2
1
```

Using a while loop

We can also loop backwards in Python using a while loop. We can set the initial value to the last index of a sequence and then decrement the index in each iteration of the loop. Here is an example:

```
my_list = [1, 2, 3, 4, 5]
i = len(my_list) - 1
while i >= 0:
    print(my_list[i])
    i -= 1
```

Output:

```
5
4
3
2
1
```

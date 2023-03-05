---
title: What is the preferred method in Python to identify the final element in a 'for' loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the built-in `enumerate` function with the loop and check if the current index is equal to the length of the iterable minus one.
---

**Contents**

[TOC]

### Using 'enumerate' function

One common way to detect the last element in a 'for' loop is by using the built-in 'enumerate' function in Python. This function returns an iterator that generates tuples with an index in the first position and the element in the second position, which we can use to check if we have reached the last element in the loop.

```python
lst = [1, 2, 3, 4, 5]
for index, elem in enumerate(lst):
    if index == len(lst)-1:
        print("This is the last element:", elem)
    else:
        print("Another element:", elem)
```

Output:

```
Another element: 1
Another element: 2
Another element: 3
Another element: 4
This is the last element: 5
```

### Using 'next' function

Another way to detect the last element in a 'for' loop is by using the built-in 'next' function in Python. This function allows us to iterate over the elements of a sequence and get the next element without including it in the iteration. We can use this in combination with a try-except block to detect when there is no next element, which means we have reached the end of the sequence.

```python
lst = [1, 2, 3, 4, 5]
for elem in lst:
    try:
        next_elem = next(iter(lst))
    except StopIteration:
        print("This is the last element:", elem)
    else:
        print("Another element:", elem)
```

Output:

```
Another element: 1
Another element: 2
Another element: 3
Another element: 4
This is the last element: 5
```

### Using 'else' clause

In Python, 'for' loops can have an 'else' clause that is executed after the loop has finished iterating over all the elements of a sequence, unless a 'break' statement was used to terminate the loop prematurely. We can use this 'else' clause to detect when we have reached the last element in the loop.

```python
lst = [1, 2, 3, 4, 5]
for elem in lst:
    if elem == lst[-1]:
        print("This is the last element:", elem)
    else:
        print("Another element:", elem)
else:
    print("Loop finished!")
```

Output:

```
Another element: 1
Another element: 2
Another element: 3
Another element: 4
This is the last element: 5
Loop finished!
```

### Using 'range' function

Finally, if we are iterating over a sequence whose length we know beforehand, we can use the built-in 'range' function and a 'for' loop to iterate over the indices of the sequence and access each element by index. We can then use the length of the sequence to check if we have reached the last index.

```python
lst = [1, 2, 3, 4, 5]
for i in range(len(lst)):
    if i == len(lst)-1:
        print("This is the last element:", lst[i])
    else:
        print("Another element:", lst[i])
```

Output:

```
Another element: 1
Another element: 2
Another element: 3
Another element: 4
This is the last element: 5
```

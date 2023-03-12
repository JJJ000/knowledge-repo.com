---
title: How can we express a "for loop" using two variables?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Yes, it is possible to have a `for loop` with two variables in Python by using the `zip` function.
---

**Contents**

[TOC]

## Using the "zip" function

One way to loop through two lists simultaneously in Python is by using the built-in `zip` function. The `zip` function takes two or more iterable objects and returns an iterator that aggregates elements from each of the iterables. We can use this iterator in a "for loop" to loop through the two lists at once.

```python
list1 = [1, 2, 3, 4]
list2 = [5, 6, 7, 8]

for x, y in zip(list1, list2):
    print(x, y)
```

Output:

```
1 5
2 6
3 7
4 8
```

## Using the "enumerate" function

Another way to loop through two variables is by using the `enumerate` function. The `enumerate` function takes an iterable object and returns an iterator that yields pairs of `(index, element)` for each element in the iterable. We can use this iterator in a "for loop" to loop through the two variables.

```python
list1 = ['a', 'b', 'c', 'd']
list2 = [1, 2, 3, 4]

for i, j in enumerate(list1):
    print(j, list2[i])
```

Output:

```
a 1
b 2
c 3
d 4
```

## Using the "range" function

If the two variables are not iterable objects or if we want to simply loop through a range of values for each variable, we can use the `range` function. The `range` function generates a sequence of numbers, starting from 0 by default, and can be used in a "for loop" to iterate through the numbers.

```python
for i in range(1, 5):
    for j in range(1, 5):
        print(i, j)
```

Output:

```
1 1
1 2
1 3
1 4
2 1
2 2
2 3
2 4
3 1
3 2
3 3
3 4
4 1
4 2
4 3
4 4
```

## Using a List of Tuples

Another way is by using a list of tuples with a "for loop". We can define a list of tuples with same length of the two variables with which we want to loop through. 

```python
list1 = ['a', 'b', 'c', 'd']
list2 = [1, 2, 3, 4]
list3 = [(x,y) for x,y in zip(list1,list2)]

for letter,number in list3:
    print(letter, number)
```

Output:

```
a 1
b 2
c 3
d 4
```

In this method, we use list comprehensions and `zip()` function to define list3. List comprehensions is a compact way to define a list without writing a `for` loop. The zip function can return a list of tuple by zipping two lists of equal length.

---
title: Can you provide an instance of the implementation of the "continue" statement in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The continue statement is used to skip over certain iterations in a loop and continue with the next iteration.
---

**Contents**

[TOC]

## Introduction

The `continue` statement is a control statement used in Python to skip the current iteration of a loop, regardless of the loop condition. The use of `continue` statement allows a programmer to save time by not executing unnecessary code in a particular iteration.

In this article, we’ll explore the various use cases of the `continue` statement with Python loop structures.

## Using `continue` with for loop

The `continue` statement can be used with a for loop to skip the current iteration and jump to the next iteration. In the following example, we use the `continue` statement to print only even numbers from a range of 0 to 10.

```python
for i in range(11):
    if i%2 != 0:
        continue
    print(i)
```

Output:

```
0
2
4
6
8
10
```

## Using `continue` with while loop

The `continue` statement can also be used with a while loop to skip the current iteration and go to the next iteration. In the example below, we use the `continue` statement to print only even numbers from a range of 0 to 10.

```python
i = 0
while i <= 10:
    i += 1
    if i%2 != 0:
        continue
    print(i)
```

Output:

```
2
4
6
8
10
```

## Skipping a specific iteration

The `continue` statement can be used to skip a specific iteration based on a condition. For instance, in the following example, we skip iteration 2 of the for loop.

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

Output:

```
0
1
3
4
```

## Conclusion

The `continue` statement is an important control statement in Python, allowing you to skip certain iterations and save time. It can be used with both for and while loops, and it’s also possible to skip a specific iteration based on certain conditions.

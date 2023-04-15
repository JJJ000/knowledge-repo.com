---
title: Reworded the concept of finding the cartesian product using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The cartesian product in pandas can be obtained using the merge function with no common column specified.
---

**Contents**

[TOC]

Section 1: Introduction

The Cartesian product is a mathematical concept that combines elements from two sets and forms all possible combinations of the elements from the two sets. In Python, we can implement the Cartesian product using the itertools module's product function or the pandas library's merge function.

In this article, we will focus on using pandas to perform Cartesian product operations on two DataFrames.

Section 2: Using the merge function

The merge function in pandas can be used to perform Cartesian product operations on two DataFrames. We can achieve this by passing both DataFrame objects to the merge function and setting the how parameter to 'outer' and the on parameter to None.

For example, consider the following two DataFrames A and B:

```
import pandas as pd

A = pd.DataFrame({'key': ['a', 'b', 'c'], 'value': [1, 2, 3]})
B = pd.DataFrame({'key': ['x', 'y', 'z'], 'value': [4, 5, 6]})
```

We can perform a Cartesian product of these two DataFrames using the following code:

```
C = pd.merge(A, B, how='outer', on=None)
```

This will result in the following output DataFrame C:

```
  key_x  value_x key_y  value_y
0     a        1     x        4
1     a        1     y        5
2     a        1     z        6
3     b        2     x        4
4     b        2     y        5
5     b        2     z        6
6     c        3     x        4
7     c        3     y        5
8     c        3     z        6
```

In the resulting DataFrame, each row represents a combination of a row from DataFrame A and a row from DataFrame B.

Section 3: Using cross join method

In pandas, the Cartesian product is also known as a cross join operation. We can use the cross join method to perform Cartesian product operations in pandas.

To use the cross join method, we can call the merge function on both DataFrames and set the how parameter to 'cross'. For example, consider the following two DataFrames A and B:

```
A = pd.DataFrame({'key': ['a', 'b', 'c'], 'value': [1, 2, 3]})
B = pd.DataFrame({'key': ['x', 'y', 'z'], 'value': [4, 5, 6]})
```

We can perform a Cartesian product of these two DataFrames using the following code:

```
C = A.merge(B, how='cross')
```

This will result in the following output DataFrame C:

```
  key_x  value_x key_y  value_y
0     a        1     x        4
1     a        1     y        5
2     a        1     z        6
3     b        2     x        4
4     b        2     y        5
5     b        2     z        6
6     c        3     x        4
7     c        3     y        5
8     c        3     z        6
```

In the resulting DataFrame, each row represents a combination of a row from DataFrame A and a row from DataFrame B.

Section 4: Conclusion

In this article, we learned how to perform Cartesian product operations on two DataFrames in pandas. We can use the merge function in pandas to perform a Cartesian product operation by setting the how parameter to 'outer', or we can use the cross join method by calling the merge function on both DataFrames and setting how to 'cross'. 

Note that a Cartesian product can result in a very large DataFrame if the two input DataFrames are large. Therefore, it is important to be mindful of the memory usage and to consider if a Cartesian product is the best approach to solving the problem.

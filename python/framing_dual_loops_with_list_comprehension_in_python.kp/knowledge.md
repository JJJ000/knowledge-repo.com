---
title: What is the process of constructing list comprehension in Python using two for loops?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can nest two for loops inside a list comprehension using the syntax [expression for variable1 in iterable1 for variable2 in iterable2].
---

**Contents**

[TOC]

Section 1: List comprehension basics
To understand how to frame two for loops in list comprehension, we must first understand the basics of list comprehension. In python, a list comprehension is a concise way of creating a list from an existing iterable or sequence. It consists of square brackets enclosing an expression followed by a for clause, optionally with additional for or if clauses. 

For example, a simple list comprehension to square the elements of a list would look like this:

```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = [num**2 for num in numbers]
print(squared_numbers)
```
Output:
```python
[1, 4, 9, 16, 25]
```
This is equivalent to the following for loop:
```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = []
for num in numbers:
    squared = num**2
    squared_numbers.append(squared)
print(squared_numbers)
```
Output:
```python
[1, 4, 9, 16, 25]
```

Section 2: Framing two for loops in list comprehension
Now that we understand the basics of list comprehension, we can move on to framing two for loops in a list comprehension. This is useful when we want to iterate over two lists at once or when we want to iterate over a nested list. 

The syntax for framing two for loops in list comprehension is as follows:

```python
new_list = [ expression for variable_1 in iterable_1 for variable_2 in iterable_2 ]
```

For example, consider the following code snippet that uses two for loops to create a list of tuples that contains all possible combinations of two lists:

```python
list1 = [1, 2, 3]
list2 = ['a', 'b', 'c']
combinations = [(num, char) for num in list1 for char in list2]
print(combinations)
```
Output:
```python
[(1, 'a'), (1, 'b'), (1, 'c'), (2, 'a'), (2, 'b'), (2, 'c'), (3, 'a'), (3, 'b'), (3, 'c')]
```

Section 3: Using if clause in two for loops
Sometimes we also need to filter out the data based on some condition while iterating two lists simultaneously using a list comprehension. In such scenarios, we use an if clause in the list comprehension.

The syntax for including an if clause in the list comprehension while framing two for loops is as follows:

```python
new_list = [ expression for variable_1 in iterable_1 for variable_2 in iterable_2 if condition ]
```

For example, let's filter even numbers from two lists using an if clause in a list comprehension:

```python
list1 = [1, 2, 3, 4, 5]
list2 = [6, 7, 8, 9, 10]
even_numbers = [(num1, num2) for num1 in list1 for num2 in list2 if num1 % 2 == 0 and num2 % 2 == 0]
print(even_numbers)
```
Output:
```python
[(2, 6), (2, 8), (2, 10), (4, 6), (4, 8), (4, 10)]
```

Section 4: Conclusion
Framing two for loops in a list comprehension can be a concise and efficient way of iterating over two lists. It is especially useful when we want to create a list based on all possible combinations of two lists or when we want to iterate over a nested list. We can also include an if clause to filter the data based on some condition.

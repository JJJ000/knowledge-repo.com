---
title: How to traverse a list with indices using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `enumerate()` function in a for loop to iterate through a list along with its indexes in Python.
---

**Contents**

[TOC]

### Method 1: Using range() and len() functions

One way to iterate through a list and access its index positions is to use the built-in `range()` and `len()` functions. 

```python
fruits = ["apple", "banana", "mango", "kiwi"]

for i in range(len(fruits)):
  print(i, fruits[i])
```
Output:
```
0 apple
1 banana
2 mango
3 kiwi
```
 
### Method 2: Using enumerate() function

The `enumerate()` function helps to get the index and the value of the element in a list as a tuple. We can then unpack this tuple to obtain the index and the value of the element in each iteration.

```python
fruits = ["apple", "banana", "mango", "kiwi"]

for i, fruit in enumerate(fruits):
  print(i, fruit)
```
Output:
```
0 apple
1 banana
2 mango
3 kiwi
```

### Method 3: Using zip() and range() functions

We can also use the `zip()` and `range()` functions to iterate over a list with the corresponding indexes. This method is commonly used when we want to loop over two or more lists in parallel:

```python
fruits = ["apple", "banana", "mango", "kiwi"]

for i, fruit in zip(range(len(fruits)), fruits):
    print(i, fruit)
```
Output:
```
0 apple
1 banana
2 mango
3 kiwi
```

### Method 4: Using a list comprehension

A list comprehension can also be used to iterate over a list with corresponding indexes. This method is useful if we want to create a new list based on the elements and their corresponding indexes in the original list:

```python
fruits = ["apple", "banana", "mango", "kiwi"]

new_list = [(i, fruit) for i, fruit in enumerate(fruits)]

print(new_list)
```
Output:
```
[(0, 'apple'), (1, 'banana'), (2, 'mango'), (3, 'kiwi')]
```

All of these methods provide a way to iterate over a list and access its index positions. The choice of method depends on the use case and personal preference.

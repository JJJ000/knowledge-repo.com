---
title: Utilize a function on every item in a collection
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Using the built-in map() function is one way to apply a function to each element of a list in Python.
---

**Contents**

[TOC]

## Introduction

In Python, we often need to perform the same operation on every element of a list. Manually iterating through each element of a list can be cumbersome and time-consuming. To simplify this operation, we can use functions that apply to each element of a list. In this tutorial, we will explore some of the most popular ways to apply functions to every element of a list.

## Method 1: Using a for loop

One of the most basic and straightforward ways to apply a function to each element of a list is by using a for loop. We can iterate through the list and apply the function to each element.

```python
def square(n):
    return n**2
 
numbers = [1, 2, 3, 4, 5]
squared_numbers = []
 
for number in numbers:
    squared_numbers.append(square(number))
 
print(squared_numbers)
```

The output of the above code will be:

```python
[1, 4, 9, 16, 25]
```

We define a function called `square` that squares a given number. Next, we define a list called `numbers`. Using a for loop, we iterate through each element of the list and apply the `square` function to it, adding the result to a new list called `squared_numbers`.

## Method 2: Using the map function

Python provides us with a built-in function called `map` to apply a function to each element of a list. The `map` function takes two parameters: the function we want to apply and the list we want to apply it to.

```python
def square(n):
    return n**2
 
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(square, numbers))
 
print(squared_numbers)
```

The output of the above code will be:

```python
[1, 4, 9, 16, 25]
```

We define a function called `square` that squares a given number. Next, we define a list called `numbers`. Using the `map` function, we apply the `square` function to each element of the list `numbers`, assigning the result to a new list called `squared_numbers`.

## Method 3: Using the list comprehension

Another way to apply a function to each element of a list is by using a list comprehension. List comprehensions are a concise and readable way of creating a new list by applying a function to each element of an existing list.

```python
def square(n):
    return n**2
 
numbers = [1, 2, 3, 4, 5]
squared_numbers = [square(number) for number in numbers]
 
print(squared_numbers)
```

The output of the above code will be:

```python
[1, 4, 9, 16, 25]
```

We define a function called `square` that squares a given number. Next, we define a list called `numbers`. Using a list comprehension, we apply the `square` function to each element of the list `numbers`, assigning the result to a new list called `squared_numbers`.

## Conclusion

In this tutorial, we explored three different ways to apply functions to each element of a list in Python. Each method has its advantages and disadvantages. The `for` loop is the most basic and flexible method, but it requires more code to implement. The `map` function is a built-in function that simplifies the process, but it can be less flexible compared to other methods. Finally, list comprehensions are a concise and readable way of applying functions to a list, but they can be less efficient for complex operations. Choose the method that best suits your needs based on the complexity of the operation and the structure of your code.

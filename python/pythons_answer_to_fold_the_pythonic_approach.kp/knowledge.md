---
title: What is the functional programming 'fold' function's equivalent in pythonic syntax?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The `pythonic` equivalent to the `fold` function from functional programming is the `reduce` function in Python.
---

**Contents**

[TOC]

The Pythonic Equivalent to the 'Fold' Function from Functional Programming

The Fold Function
The fold function, also known as reduce in Python, is a higher-order function that takes a binary operator and a list of elements and applies this operator to the elements in the list to reduce it to a single value. Fold is a common function in functional programming languages like Haskell, and it is also available in Python through the functools module. However, Python provides a more idiomatic way of performing this operation.

Using the 'reduce' Function
The reduce function from the functools module is an implementation of the fold function in Python. It takes two arguments: the function that performs the reduction and the iterable to be reduced. The function is applied successively to the elements of the iterable, with the result of each step becoming the left-hand argument of the next step until only a single value remains. However, reduce is not considered very Pythonic, and the preferred way of writing this function is by using a for loop.

Using a For Loop
Unlike languages like Haskell, Python emphasizes readability and simplicity, and using a for loop is the most Pythonic way of implementing the fold function. Instead of using a single line of code, Python developers prefer to use a simple for loop that explicitly performs the operation.

def foldr(f, elems, init):
    acc = init
    for elem in reversed(elems):
        acc = f(elem, acc)
    return acc

This function takes a callable operator, elems to be reduced, and an initial value. The for loop iterates through the elements in reverse order, performing the operation on each element and the current accumulated value. The final value is returned after the loop is completed.

Conclusion
In conclusion, Python has a more Pythonic way of implementing the fold function than using the reduce function from the functools module. With a simple for loop, Python developers can create a readable and explicit implementation that performs the same operation as fold. By writing code in a way that is more in line with Python's philosophy of code readability and simplicity, developers can make their code more maintainable and scalable.

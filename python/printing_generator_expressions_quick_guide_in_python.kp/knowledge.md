---
title: What are the steps involved in printing a generator expression?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Wrap the generator expression within a print statement or iterate over the generator using a loop.
---

**Contents**

[TOC]

## Introduction
In Python, a generator expression is a convenient way to generate a series of values on the fly. It is very useful when working with a large number of values, as it generates the values lazily and doesn't store them in memory. However, sometimes we may want to print the values generated by a generator expression. In this tutorial, we will show you how to print a generator expression in Python.

## Using a for loop
The simplest way to print the values generated by a generator expression is to use a for loop. We can iterate over the generator expression and print each value that is generated. Here's an example:

```python
gen_expr = (x for x in range(10))
for val in gen_expr:
    print(val)
```

In this example, we have created a generator expression that generates the integers from 0 to 9. We then loop over the generator expression using a for loop, and print each value that is generated. Note that once all the values have been generated, the generator expression will stop generating values.

## Using the list() function
Another way to print the values generated by a generator expression is to convert the generator expression into a list using the list() function. Here's an example:

```python
gen_expr = (x for x in range(10))
print(list(gen_expr))
```

In this example, we have created a generator expression that generates the integers from 0 to 9. We then convert the generator expression into a list using the list() function and print the resulting list. This will print all the values generated by the generator expression.

## Using the join() method
If a generator expression generates strings, we can use the join() method to concatenate the strings and print them. Here's an example:

```python
gen_expr = (str(x) for x in range(10))
print(' '.join(gen_expr))
```

In this example, we have created a generator expression that generates strings representing the integers from 0 to 9. We then use the join() method to concatenate the strings with a space separator and print the resulting string. This will print all the values generated by the generator expression separated by a space.

## Conclusion
In this tutorial, we have shown you three different ways to print a generator expression in Python. You can use a for loop to iterate over the generator expression and print each value, convert the generator expression into a list and print the resulting list, or use the join() method to concatenate the strings generated by the generator expression and print the resulting string.
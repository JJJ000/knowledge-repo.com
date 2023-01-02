---
title: What does the "yield" keyword do in Python? 
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/thumbnail.png
created_at: 2022-12-30 00:00:00
updated_at: 2022-12-31 00:00:00
tldr: "yield" is used in the body of a function like a return statement, but instead of returning a value and terminating the function, it yields a value and suspends the function's execution, which makes it an efficient way to implement iterators.
---

**Contents**

[TOC]

### Yield in Python

In Python, the `yield` keyword is used in the body of a function like a return statement, but instead of returning a value and terminating the function, it yields a value and suspends the function's execution. The function can then be resumed later on, allowing it to generate a sequence of values over time, rather than computing them all at once and returning them in a list, for example. This makes it an efficient way to implement iterators, which are objects that allow you to loop over a sequence of values, one at a time.

### Examples

Here is an example of a simple generator function that uses the `yield` keyword to yield a sequence of numbers:

```Python
def count_up_to(max):
    count = 1
    while count <= max:
        yield count
        count += 1

for number in count_up_to(5):
    print(number)
```

This would output the following:

```
1
2
3
4
5
```

Here is a more advanced example of a generator function that uses the `yield` keyword to yield a sequence of Fibonacci numbers:

```Python
def fibonacci(max):
    a, b = 0, 1
    while a < max:
        yield a
        a, b = b, a + b

for number in fibonacci(1000):
    print(number)
```

This generator function uses a while loop to generate a sequence of Fibonacci numbers that are less than the maximum value specified by the caller. On each iteration of the loop, it yields the current value of `a` and then updates `a` and `b` with the next two values in the sequence.

This generator function can be used like this:

```Python
for number in fibonacci(1000):
    print(number)
```

This would output the following sequence of Fibonacci numbers:

```
0
1
1
2
3
5
8
13
21
34
55
89
144
233
377
```

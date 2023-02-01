---
title: What steps are needed to construct a basic iterator?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Create a class that implements the \_\_iter\_\_ and \_\_next\_\_ methods.
---

**Contents**

[TOC]

## Section 1: Defining the Iterator

An iterator is an object that can be used to iterate over a collection of items. In Python, an iterator is created by implementing the `__iter__` and `__next__` methods.

The `__iter__` method is called when an iterator is created and it should return the iterator object itself. This allows the iterator to be used in a `for` loop.

The `__next__` method is called each time the `next()` function is called on the iterator. This method should return the next item in the collection. If there are no more items to be returned, it should raise a `StopIteration` exception.

## Section 2: Creating a Basic Iterator

To create a basic iterator, we can define a class that implements the `__iter__` and `__next__` methods. The `__iter__` method should return the iterator object itself, and the `__next__` method should return the next item in the collection.

For example, we can create an iterator for a list of numbers:

```python
class NumberIterator:
    def __init__(self, numbers):
        self.numbers = numbers
        self.index = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.index >= len(self.numbers):
            raise StopIteration
        number = self.numbers[self.index]
        self.index += 1
        return number
```

## Section 3: Using the Iterator

Once the iterator has been defined, it can be used in a `for` loop. For example:

```python
numbers = [1, 2, 3, 4, 5]

iterator = NumberIterator(numbers)
for number in iterator:
    print(number)
```

This will print out each number in the list.

## Section 4: Advanced Iterators

The basic iterator defined above is a simple example of how to create an iterator in Python. There are more advanced techniques that can be used to create more sophisticated iterators, such as using generators or using the `itertools` module.

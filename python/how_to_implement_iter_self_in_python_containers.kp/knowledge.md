---
title: What is the procedure for implementing __iter__(self) in a Python container object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Return an iterator object that defines the \_\_next\_\_() method and raises StopIteration when there are no more elements.
---

**Contents**

[TOC]

Section 1: Introduction
When implementing container objects in Python, it is often necessary to make them iterable. In order to do so, the container class must define an __iter__(self) method that returns an iterator object.

Section 2: Creating an Iterator Class
To implement __iter__(self), we first need to create an iterator class that defines the __next__(self) method. This method should return the next value in the sequence and raise a StopIteration exception when the sequence is exhausted.

```
class MyIterator:
    def __init__(self, data):
        self.index = 0
        self.data = data

    def __iter__(self):
        return self

    def __next__(self):
        if self.index >= len(self.data):
            raise StopIteration
        result = self.data[self.index]
        self.index += 1
        return result
```

In this example, we create an iterator class, MyIterator, that takes a sequence of data as an argument. The __iter__(self) method returns the iterator object (in this case, the instance of MyIterator itself), and the __next__(self) method returns the next value in the sequence.

Section 3: Implementing __iter__(self)
Once we have an iterator class, implementing __iter__(self) in the container class is straightforward. We simply create an instance of the iterator class and return it from __iter__(self).

```
class MyContainer:
    def __init__(self, data):
        self.data = data

    def __iter__(self):
        return MyIterator(self.data)
```

In this example, we define a container class, MyContainer, that takes a sequence of data as an argument. The __iter__(self) method creates an instance of MyIterator with the data and returns it.

Section 4: Using the Iterable Container
Once the container class has implemented __iter__(self), we can use it with for loops and other tools that expect iterable objects.

```
my_container = MyContainer([1, 2, 3, 4, 5])
for value in my_container:
    print(value)

# Output:
# 1
# 2
# 3
# 4
# 5
```

In this example, we instantiate MyContainer with a list of numbers and then iterate over the container using a for loop. The __next__(self) method of the MyIterator instance created by __iter__(self) is called repeatedly until the StopIteration exception is raised, at which point the loop ends.

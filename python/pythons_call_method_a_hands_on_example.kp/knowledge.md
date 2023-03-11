---
title: A practical application of the Python special method __call__ can be demonstrated by
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The \_\_call\_\_ special method allows instances of a class to be callable like a function.
---

**Contents**

[TOC]

# Introduction to the __call__ method
The `__call__` method in Python is a special method that can be implemented in a class to enable the class instances to be treated as functions. This method is called when the instance of the class is called as a function. In this article, we will discuss the practical example of how to use the `__call__` method in Python.

# Practical example of using the __call__ method
Consider the following example of a class that implements the `__call__` method:
```python
class Multiplier:
    def __init__(self, factor):
        self.factor = factor

    def __call__(self, x):
        return self.factor * x
```
In the above code, we have defined a class called `Multiplier` that takes a parameter `factor` and initializes it using the constructor. The `__call__` method is implemented in the class which takes a parameter `x` and returns the product of `factor` and `x`.

# Using the Multiplier class
To use the `Multiplier` class, we need to create an instance of the class and call it as a function. The following code demonstrates how to use the `Multiplier` class:
```python
m = Multiplier(10)
result = m(5)

print(result) # Output: 50
```
In the above code, we have created an instance of the `Multiplier` class with a factor of `10`. We then called the instance as a function with a value of `5`. The output of the program is `50`, which is the product of `10` and `5`.

# Practical application of the __call__ method
The `__call__` method can be used in many practical applications, such as implementing function-like behavior in classes. This can be useful in situations where we need to encapsulate some behavior in a class and make it available as a callable object.

For example, we can use the `__call__` method to create a class that implements a simple timer. The class can take a start time and provide a method to calculate the elapsed time.

```python
import time

class Timer:
    def __init__(self):
        self.start_time = None

    def __call__(self):
        if self.start_time is None:
            self.start_time = time.time()
        else:
            return time.time() - self.start_time
```

In the above code, we have defined a class called `Timer` that has an instance variable called `start_time`. The `__call__` method is implemented in the class which checks if the `start_time` is initialized, if not, it initializes it with the current time. If `start_time` is already initialized, it returns the difference between the current time and `start_time`, which gives us the elapsed time.

# Conclusion
In this article, we have seen the practical example of using the `__call__` method in Python. We have also discussed how to use the `__call__` method to implement function-like behavior in classes and demonstrated a practical application of the `__call__` method. The `__call__` method is a powerful tool in the Python language that can help us create callable objects that can be treated as functions.

---
title: How to access a class property in Python using a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can access a class property from a string using the built-in function `getattr()`.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, accessing class properties from a string can be achieved using the built-in `getattr()` function. This function takes two arguments: the first one is the instance of the class which we want to access the property from, and the second one is a string that represents the name of the desired property.

Section 2: Example
Let's demonstrate this with an example. Suppose we have a class called `Person` with properties such as `name`, `age`, and `gender`. To access the `age` property of an instance of `Person` named `john`, we can use the following code snippet:

```
class Person:
  def __init__(self, name, age, gender):
    self.name = name
    self.age = age
    self.gender = gender

john = Person("John", 30, "male")

age = getattr(john, "age")

print(age)
```

Here, we accessed the `age` property of the `john` instance of `Person` using the `getattr()` function and passed `john` and `"age"` as its arguments.

Section 3: Handling errors
It is important to note that if the property name provided to `getattr()` does not exist in the class, it will raise an `AttributeError` exception. To handle this exception, we can either use a `try-except` block or provide a default value as the third argument to `getattr()`.

```
class Person:
  def __init__(self, name, age, gender):
    self.name = name
    self.age = age
    self.gender = gender

john = Person("John", 30, "male")

try:
  phone = getattr(john, "phone")
except AttributeError:
  print("Phone property does not exist")

address = getattr(john, "address", "N/A")

print(address)
```

Here, we tried to access a non-existing `phone` property of the `john` instance of `Person`. The `try-except` block handles the `AttributeError` exception raised by `getattr()`. We also provided a default value of `"N/A"` for the non-existing property name `address`.

Section 4: Conclusion
In conclusion, accessing class properties from a string in Python is achievable using the `getattr()` function. It is important to handle exceptions when accessing non-existing properties using `try-except` blocks or providing default values.

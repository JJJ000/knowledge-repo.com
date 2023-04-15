---
title: The use of type annotations in named tuples
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Type hints can be added to a namedtuple in Python using the `typing` module.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
In python, Namedtuple is a subclass of tuple which is used to create tuple-like objects that have fields accessible by attributes as well as indexes. These namedtuples are immutable which means that their values cannot be changed. In this document, we will discuss how type hints can be added to namedtuples in python 3.6 and above.


Section 2: Adding Type Hints to Namedtuples
------------------------------------------
Type hints are used to specify the expected type of a variable, function parameter or return value. In namedtuples, these type hints can be added as keyword arguments to the namedtuple() constructor.

For example, consider the following named tuple:

```
from typing import NamedTuple

class Employee(NamedTuple):
    name: str
    age: int
    salary: float
```

Here, we have created an Employee namedtuple with three fields: name, age and salary. The type hints for these fields are: str, int and float respectively.

Once the type hints are added, it becomes easier to understand the expected type of the values stored in the namedtuple fields. This is especially useful in large codebases where understanding the expected types of variables and function parameters can be a challenge.


Section 3: Using Type Hints in Namedtuples
-----------------------------------------
Type hints can be used in a number of ways when using namedtuples. For example, when creating a new instance of a namedtuple, we can use the named fields to initialize the object as shown below:

```
emp_1 = Employee(name='John', age=30, salary=10000.00)
emp_2 = Employee(name='Mike', age=35, salary=15000.00)
```

Here, we have created two instances of the Employee namedtuple and initialized their fields using the named fields.

Type hints can also be used in function parameters and return types. Consider the following example:

```
def get_employee_name(emp: Employee) -> str:
    return emp.name
```

Here, we have defined a function get_employee_name() which takes an Employee named tuple as input and returns its name as a string. The type hints for the function parameters and return types make it clear what type of values can be expected in the function.


Section 4: Conclusion
---------------------
Namedtuples are a useful way to create tuple-like objects with named fields. By adding type hints to these namedtuples, we can make our code more understandable and maintainable. Type hints can be used not only when creating namedtuple objects, but also in function parameters and return types. The use of type hints is especially helpful in larger codebases where understanding the expected types of variables and function parameters can be a challenge.

---
title: What is the process of converting an integer to an enumeration in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can convert an integer to an Enum in Python using the Enum class method `Enum(int\_value)`.
---

**Contents**

[TOC]

Section 1: Enum Definition
-------------------------
First, we need to define the enum using the Enum class from the enum module. For this, we can create an Enum class called MyEnum and add some enumeration members using the auto() function as follows:

```python
from enum import Enum, auto

class MyEnum(Enum):
    FIRST = auto()
    SECOND = auto()
    THIRD = auto()
```

Here, we have defined an enum called MyEnum with three enumeration members: FIRST, SECOND, and THIRD. We have used the auto() function to automatically generate unique values for each member.


Section 2: Converting int to Enum member
---------------------------------------
Now, we need to convert an integer value to an enum member. For this, we can define a function called int_to_enum that takes an integer value and returns the corresponding enum member using the value attribute of the enum members as follows:

```python
def int_to_enum(value):
    for member in MyEnum:
        if member.value == value:
            return member
```

This function iterates over all the members of the MyEnum enum class and checks if the value attribute of the member is equal to the given value. If it is, the function returns the member.


Section 3: Using the int_to_enum function
----------------------------------------
To use the int_to_enum function, we can simply call it with the integer value we want to convert as follows:

```python
value = 2
member = int_to_enum(value)
print(member)
```

Here, we have assigned the value 2 to the variable value and called the int_to_enum function with this value. The function returns the enum member corresponding to this value, which is the member MyEnum.THIRD. We have assigned this member to the variable member and printed it.


Section 4: Complete code
------------------------
Here is the complete code for the enum definition, the int_to_enum function, and an example usage:

```python
from enum import Enum, auto

class MyEnum(Enum):
    FIRST = auto()
    SECOND = auto()
    THIRD = auto()

def int_to_enum(value):
    for member in MyEnum:
        if member.value == value:
            return member

value = 2
member = int_to_enum(value)
print(member)
```

This code will output:

```
MyEnum.THIRD
```

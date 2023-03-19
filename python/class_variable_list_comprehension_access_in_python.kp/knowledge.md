---
title: Using list comprehension inside a class definition to retrieve class variables
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can access class variables directly in a list comprehension within the class definition by using the class name followed by the variable name, like so [MyClass.my\_var for obj in my\_list].
---

**Contents**

[TOC]

Section 1: Definition of Class Variables
In Python, class variables are variables that are declared inside the class definition, but outside of any methods. They are shared across all instances of the class and can be accessed using the class name or any instance of the class.

Section 2: Using Class Variables in a List Comprehension
To access class variables from within a list comprehension in the class definition, you can use the class name directly instead of using self. This is because the list comprehension is executed in the context of the class namespace, rather than the instance namespace.

For example, let's assume we have a class with a class variable called "nums":

```python
class MyClass:
    nums = [1, 2, 3, 4, 5]

    def double_nums(self):
        return [x * 2 for x in MyClass.nums]
```

In this code, the "double_nums" method uses a list comprehension to iterate over the "nums" class variable and return a new list where each value is doubled. Note that we have used "MyClass.nums" instead of "self.nums" to access the class variable.

Section 3: Using Class Variables in a List Comprehension with Inheritance
If the class with the list comprehension inherits from another class that also has a class variable with the same name, you can access the parent class variable using the super() function.

For example:

```python
class ParentClass:
    nums = [1, 2, 3]

class ChildClass(ParentClass):
    nums = [4, 5, 6]

    def double_nums(self):
        parent_nums = super().nums
        child_nums = [x * 2 for x in self.nums]
        return parent_nums + child_nums
```

In this code, the "double_nums" method of the ChildClass first calls the "nums" class variable from the parent class using "super().nums" and stores it in the "parent_nums" variable. It then accesses the "nums" class variable of the child class using "self.nums" and doubles its values using a list comprehension.

Section 4: Conclusion
To summarize, class variables can be accessed directly in a list comprehension in the class definition using the class name. If using inheritance, the parent class variable can be accessed using the "super()" function. By understanding these concepts, you can easily manipulate class variables using list comprehension in Python.

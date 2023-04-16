---
title: What is the syntax for printing instances of a class using print()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can print instances of a class using the print() function by passing the instance as an argument.
---

**Contents**

[TOC]

# Section 1: Define the Class

Before you can print instances of a class, you must first define the class. To do this, use the `class` keyword followed by the name of the class. Then, define the class's attributes and methods within the class's code block.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def say_hello(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")
```

# Section 2: Create Instances

Once the class is defined, you can create instances of the class. To do this, use the class name followed by parentheses containing the desired arguments. 

```python
bob = Person("Bob", 25)
alice = Person("Alice", 30)
```

# Section 3: Print Instances

Now that you have created instances of the class, you can print them using the built-in `print()` function.

```python
print(bob)
print(alice)
```

# Section 4: Output

The output of the above code will be the memory address of the instances.

```
<__main__.Person object at 0x7f8b4b6b9f90>
<__main__.Person object at 0x7f8b4b6b9fd0>
```

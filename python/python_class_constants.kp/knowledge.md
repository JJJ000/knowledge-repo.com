---
title: Python's constants that belong to a particular class
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Class constants in Python are variables that are defined within a class and have a fixed value that cannot be modified throughout the program.
---

**Contents**

[TOC]

Section 1: Introduction to Class Constants
Class constants refer to a set of fixed values defined within a class that can be accessed throughout the class without being mutated. These values do not change during the execution of the program and are used to store data or parameters that represent the characteristics or requirements of the object class.

Section 2: Declaring Class Constants
To declare class constants in Python, we use the 'const' keyword followed by the constant name and assignment operator. We then assign the value to the constant. Here is an example:

```
class Example:
    const_name = 10
```

In this example, we define a class 'Example' and declare a constant 'const_name' with the value of 10. The constant can now be accessed and used anywhere in the class.

Section 3: Using Class Constants
We can use class constants in the same way as we use other class attributes. We can access them using either the class name or the instance of the class. Here is an example:

```
class Example:
    const_name = 10
    
    def __init__(self, value):
        self.value = value 
        
    def display(self):
        print("Class constant value: ", Example.const_name)
        print("Instance variable value: ", self.value)
```

In this example, we declare a class 'Example' with a constant 'const_name' and a parameterized constructor 'init'. We then define a method 'display' that displays both the class constant value and the instance variable value. We can access the class constant by using 'Example.const_name' or 'self.const_name' as follows:

```
example = Example(20)
example.display()
```

Output:
```
Class constant value: 10
Instance variable value: 20
```

Section 4: Advantages of Using Class Constants
Using class constants provides numerous benefits, such as improving code readability, reducing redundancy, and easing code maintenance. They also ensure that the data stored in the constant remains consistent throughout the class and cannot be accidentally modified during execution. Furthermore, class constants are accessible anywhere in the class, making it easy to reference and utilize them.

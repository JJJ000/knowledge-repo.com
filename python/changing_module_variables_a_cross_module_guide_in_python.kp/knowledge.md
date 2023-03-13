---
title: What is the method for modifying a module variable from a different module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can change a module variable from another module in Python by importing the first module and using dot notation to access and modify the variable.
---

**Contents**

[TOC]

# Approach

There are a few approaches that can be taken to change a module variable from another module in Python. Below are four possible methods: 

1. Import the module and modify the variable directly
2. Use a function in the first module to modify the variable and call it from the second module
3. Use a class in the first module to modify the variable and call its methods from the second module
4. Use a global variable in the first module that can be accessed and modified from the second module


## Method 1: Directly modify the variable

One approach is to import the module and modify the variable directly. For example, if we have a module `module1` with a variable `var1` that we want to modify from `module2`, we can simply import `module1` in `module2` and set `module1.var1` to a new value. 

```python
# module1.py

var1 = "hello"


# module2.py

import module1

module1.var1 = "world"
```

After this code is executed, `var1` in `module1` will now be set to `"world"`.



## Method 2: Use a function to modify the variable

Another approach is to write a function in `module1` that modifies the variable, and call that function from `module2`. This can be useful if the modification requires more complex logic than simply assigning a new value. 

```python 
# module1.py

def modify_var(new_val):
    global var1
    var1 = new_val


# module2.py

import module1

module1.modify_var("hello")
```

In this example, we define a function `modify_var()` in `module1` that sets `var1` to a new value. We then import `module1` in `module2` and call `modify_var()` with the desired new value.



## Method 3: Use a class to modify the variable

Similar to using a function, we can also use a class to modify the variable. This can make more sense if we have multiple variables that need to be modified in a coordinated way. 

```python
# module1.py

class MyClass:
    def __init__(self, var_val):
        self.var1 = var_val

    def modify_var(self, new_val):
        self.var1 = new_val


# module2.py

import module1

obj = module1.MyClass("hello")
obj.modify_var("world")
```

Here we define a class `MyClass` that has a variable `var1`, and a method `modify_var()` that sets `var1` to a new value. We create an instance of `MyClass` in `module2` and call the `modify_var()` method to change its value.



## Method 4: Use a global variable

Finally, we can use a global variable in `module1` that can be accessed and modified from `module2`. This method is generally discouraged due to potential issues with variable scoping and unintended side effects, but it can be useful in some contexts. 

```python
# module1.py

global_var = "hello"


# module2.py

import module1

module1.global_var = "world"
```

Here we define a global variable `global_var` in `module1`, which can be accessed and modified directly from `module2`. Again, this method is generally not recommended due to its potential for unintended side effects and difficulty in tracking down issues.

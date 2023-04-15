---
title: Can you suggest the quickest method to verify if a class has a defined function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the built-in function `hasattr(class\_name, `function\_name`)` to check if the class has the specified function.
---

**Contents**

[TOC]

## Section 1: Understanding the hasattr() function

In Python, we can use the built-in hasattr() function to check if an object has a specific attribute or method. This function takes two arguments: the object to be checked, and the name of the attribute or method in string format.

The hasattr() function returns a boolean value, True if the attribute or method is present, False otherwise. Therefore, we can use this function to quickly check if a class has a particular function defined.


## Section 2: Implementing hasattr() to check for a function in a class

To use hasattr() to check for the presence of a function in a class, we need to pass the class object as the first argument, and the name of the function as a string in the second argument.

Here's an example code snippet:

```python
class MyClass:
    def my_function(self):
        print("Hello world")

# Check if MyClass has a function called "my_function"
if hasattr(MyClass, "my_function"):
    print("MyClass has my_function")
else:
    print("MyClass does not have my_function")
```

In this example, we define a class called MyClass with a single function called my_function(). We then use hasattr() to check if the class has the method called "my_function". If it does, we print a message indicating this. Otherwise, we print a message indicating that the function is not present in the class.


## Section 3: Conclusion

In conclusion, the fastest way to check if a class has a function defined in Python is to use the built-in hasattr() function. This function takes the class object and the function name as arguments, and returns a boolean value indicating whether the function is present or not. With this simple check, we can quickly determine whether a class has a specific function or not.

---
title: Is there a way to verify whether my Python object is a numerical value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the isinstance() function to check if the object is an instance of the numeric types (int, float, complex, etc.).
---

**Contents**

[TOC]

## Method 1: Using isinstance() function

One easy way to check whether a Python object is a number or not is by using the built-in function isinstance(). We can provide the object to be checked as the first argument and the type we want to check for as the second argument. If the object is of the specified type, it will return True, otherwise False.

```python
# Example code using isinstance()

x = 5
y = 'hello'
z = 3.14

print(isinstance(x, int))       # True
print(isinstance(y, int))       # False
print(isinstance(z, (int, float)))  # True
```

In this example code, we first create three different objects of different types. Then we use the isinstance() function to check if each is a number. We check if x is of type int and it returns True. We check if y is of type int and it returns False. We check if z is either of type int or float, and it returns True.


## Method 2: Using type() function

Another way to check whether an object is a number or not is to use the type() function. We can simply use the type() function on the object and check if it belongs to any of the numerical types in Python.

```python
# Example code using type()

x = 5
y = 'hello'
z = 3.14

print(type(x) in [int, float, complex])    # True
print(type(y) in [int, float, complex])    # False
print(type(z) in [int, float, complex])    # True
```

In this example code, we use the type() function to check if x, y, and z are of any of the numerical types. We check if the types of x and z belong to the list containing int, float, and complex. Since both x and z have either int or float type, it returns True. However, y does not belong to any of the numerical types, so it returns False.


## Method 3: Using hasattr() function

We can also check if an object is a number using the hasattr() function. This function is primarily used to check if an object has a specific attribute, but we can also use it to check if an object has a numeric type.

```python
# Example code using hasattr()

x = 5
y = 'hello'
z = 3.14

print(hasattr(x, '__int__'))        # True
print(hasattr(y, '__int__'))        # False
print(hasattr(z, '__int__'))        # True
```

In this example code, we use the hasattr() function to check if x, y, and z are numeric types. We check if x and z have the '__int__' attribute, which is present in all numeric types such as int, float, complex, etc. Therefore, it returns True for both x and z. However, y does not have the attribute '__int__', so it returns False.


## Method 4: Using try-except block

Finally, we can also check if an object is a number using a try-except block. We can try to cast the object to a numeric type and catch any exceptions that may occur if it's not a number.

```python
# Example code using try-except block

x = 5
y = 'hello'
z = 3.14

try:
    int(x)
    print('x is a number.')
except ValueError:
    print('x is not a number.')

try:
    int(y)
    print('y is a number.')
except ValueError:
    print('y is not a number.')

try:
    int(z)
    print('z is a number.')
except ValueError:
    print('z is not a number.')
```

In this example code, we use a try-except block to check if x, y, and z are numbers. We try to cast each object to an int type using the int() function, which will raise a ValueError exception if it's not a number. If the exception is caught, we print a message saying the object is not a number, otherwise, we print a message saying it is a number. In this case, x and z are numbers, so they print "x/z is a number." However, y is not a number, so it prints "y is not a number."

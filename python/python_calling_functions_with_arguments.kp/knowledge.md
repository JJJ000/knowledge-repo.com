---
title: Invoke a function in Python by passing an argument list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To call a function with argument list in Python, you can pass the arguments as a comma-separated list enclosed in parentheses after the function name.
---

**Contents**

[TOC]

## Defining a Function

Before we can call a function with argument list in Python, we first need to define a function. 

```python
def my_function(arg1, arg2, arg3):
    # function code here
```

In this example, we are defining a function called `my_function` that takes in three arguments (`arg1`, `arg2`, and `arg3`). The function code goes inside the block after the `:`. 


## Calling a Function with Argument List

Once we have defined our function, we can call it with argument list by passing the values of the arguments inside the parentheses.

```python
my_function(value1, value2, value3)
```

For example, to call our `my_function` with the values `1`, `"hello"`, and `True`, we would use:

```python
my_function(1, "hello", True)
```


## Handling Arguments in a Function

Inside the function, we can use the argument values in any way that we want. For example:

```python
def my_function(arg1, arg2, arg3):
    print(f"The first argument is {arg1}")
    print(f"The second argument is {arg2}")
    print(f"The third argument is {arg3}")
```

When we call this function with the values we used earlier, we will get the following output:

```
The first argument is 1
The second argument is hello
The third argument is True
```


## Default and Optional Arguments

In Python, we can also define default or optional arguments for functions. These arguments have a default value assigned, and if no argument is passed when calling the function, the default value is used.

```python
def my_function(arg1, arg2="default_value", arg3=42):
    # function code here
```

In this example, we have defined the arguments `arg2` and `arg3` with default values. We can call this function with only the required argument `arg1`, like this:

```python
my_function("hello")
```

This will use the default values for `arg2` and `arg3`. We can also pass new values for `arg2` and `arg3` like this:

```python
my_function("hello", "new_value", 123)
``` 

This will use the new values we passed for `arg2` and `arg3`.

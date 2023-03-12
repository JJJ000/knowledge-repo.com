---
title: The act of employing a string variable for the purpose of identifying a variable
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: It is not possible to use a string variable as a variable name in Python.
---

**Contents**

[TOC]

Introduction: 

Python is a dynamically typed language. It allows us to create variables on the fly without the need for defining a data type at the time of declaration. This feature can be used to create dynamic variable names. To be precise, it’s a matter of using a string variable as a variable name in Python.


Using Eval function: 

The eval() function in python is used to execute a python expression in a string. We can use this function to create dynamic variable names.

Syntax: 

eval('variable_name' +  ' = ' + 'value’)

Here, the ‘variable_name’ and ‘value’ are a string that represents a variable name and its value, respectively.

Example: 

variable_name = "x"
value = 5
eval(variable_name + ' = ' + str(value))
print(x) 

This will create a variable named x and assign it with a value of 5. The print statement will output the value of the variable x which is 5.


Using Dictionary: 

Python dictionaries are used to store key-value pairs. We can use dictionaries to create dynamic variable names.

Syntax: 

variables = {}
variables[‘variable_name’] = value

Here, ‘variable_name’ represents the key and ‘value’ represents its value.

Example: 

variables = {}
variable_name = "x"
value = 5
variables[variable_name] = value
print(variables['x'])

This will create a dictionary variable named ‘variables’. We are assigning the value 5 to its key ‘x’. The print statement will output the value of the key ‘x’ which is 5.


Using the globals() function: 

The globals() function in Python returns a dictionary containing the current global symbol table. We can use this dictionary to create dynamic variable names.

Syntax: 

globals()[‘variable_name’] = value

Here, ‘variable_name’ represents the key and ‘value’ represents its value.

Example: 

variable_name = "x"
value = 5
globals()[variable_name] = value
print(x)

This will create a global variable named ‘x’ and assign it a value of 5. The print statement will output the value of the global variable ‘x’ which is 5.

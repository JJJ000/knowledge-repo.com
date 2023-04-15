---
title: Incorporating a function into an existing object instance
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can add a method to an existing object instance in Python by assigning a function to the object`s \_\_dict\_\_ attribute.
---

**Contents**

[TOC]

#### Defining the Method

The first step is to define the method that will be added to the existing object instance. This is done by defining a function that takes the object instance as an argument and performs the desired action. For example, if we wanted to add a method to a string object instance that returns the length of the string, the method could be defined as follows:

```python
def string_length(string_instance):
    return len(string_instance)
```

#### Binding the Method to the Object

Once the method is defined, it needs to be bound to the object instance. This can be done by using the built-in `setattr` function. This function takes three arguments: the object instance, the name of the method, and the function that defines the method. For example, to bind the `string_length` method to a string object instance, the following code could be used:

```python
string_instance = 'example'
setattr(string_instance, 'string_length', string_length)
```

#### Using the Method

Once the method is bound to the object instance, it can be used just like any other method. For example, if the `string_length` method was bound to the `string_instance` object, it could be used like this:

```python
string_length = string_instance.string_length()
print(string_length) # prints 7
```

#### Removing the Method

Finally, if the method needs to be removed from the object instance, the built-in `delattr` function can be used. This function takes two arguments: the object instance and the name of the method. For example, to remove the `string_length` method from the `string_instance` object, the following code could be used:

```python
delattr(string_instance, 'string_length')
```

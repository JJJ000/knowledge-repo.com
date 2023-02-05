---
title: What is the process for creating an object and adding attributes to it?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can create an object and add attributes to it in Python by using the dot notation (object.attribute = value).
---

**Contents**

[TOC]

**Creating an Object**

To create an object in Python, you can use the `class` keyword. For example:

```python
class MyObject:
    pass
```

This creates a class called `MyObject`, which can be used to create an object.

**Adding Attributes to an Object**

Once you have created an object, you can add attributes to it. This is done by assigning values to the attributes within the class definition. For example:

```python
class MyObject:
    name = "MyObject"
    color = "red"
```

This creates an object with two attributes, `name` and `color`, and assigns them the values `"MyObject"` and `"red"`, respectively.

**Creating an Instance of an Object**

To create an instance of an object, you can use the `MyObject()` constructor. This will create an instance of the `MyObject` class, with the attributes and values specified in the class definition. For example:

```python
my_object = MyObject()
```

This creates an instance of the `MyObject` class, with the `name` and `color` attributes set to `"MyObject"` and `"red"`, respectively.

**Accessing an Object's Attributes**

Once you have created an instance of an object, you can access its attributes using the `.` operator. For example:

```python
my_object_name = my_object.name
my_object_color = my_object.color
```

This will assign the `name` and `color` attributes of `my_object` to the variables `my_object_name` and `my_object_color`, respectively.

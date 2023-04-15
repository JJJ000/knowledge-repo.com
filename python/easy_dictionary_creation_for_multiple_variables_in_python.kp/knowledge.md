---
title: What is a more straightforward approach to generating a dictionary with individual variables?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can create a dictionary of separate variables in Python by using the dictionary comprehension method.
---

**Contents**

[TOC]

Using the dict() constructor

One simple way to create a dictionary of separate variables in Python is to use the dict() constructor. First, define each variable and its corresponding value, then pass them as arguments to the dict() constructor. For example:

```python
name = "Alice"
age = 25
occupation = "Software Developer"

person_dict = dict(name=name, age=age, occupation=occupation)
```

Using dictionary comprehension

Another way to create a dictionary of separate variables is to use dictionary comprehension. This method is particularly useful when you have many variables to define. Here's an example:

```python
variables = {
    "name": "Alice",
    "age": 25,
    "occupation": "Software Developer"
}

person_dict = {key: value for key, value in variables.items()}
```

Using the vars() function

If your variables are defined as attributes of an object, you can use the vars() function to create a dictionary of those variables. For example:

```python
class Person:
    def __init__(self, name, age, occupation):
        self.name = name
        self.age = age
        self.occupation = occupation

person = Person("Alice", 25, "Software Developer")
person_dict = vars(person)
```

Using locals() function

The locals() function returns a dictionary containing the current scope's local variables and their values. We can use this function to create a dictionary of separate variables in Python. Here's an example:

```python
name = "Alice"
age = 25
occupation = "Software Developer"

person_dict = {k:v for k,v in locals().items() if k != "person_dict"}
```

Here, we're passing a dictionary comprehension to `person_dict` which filters out the dictionary itself, i.e. `person_dict`, from the local `locals()`.

---
title: What is the process for transforming a nested Python dictionary into an object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the built-in `dict` class to convert a nested Python dict to an object.
---

**Contents**

[TOC]

### Section 1 - Overview

A nested Python dict can be converted to an object by creating a class that contains the dict's keys and values as class attributes. The class methods can then be used to access and modify the dict values.

### Section 2 - Creating the Class

The first step in converting a nested Python dict to an object is to create a class that contains the dict's keys and values as class attributes. The class should have a constructor that takes in the dict as an argument and assigns each key-value pair to a class attribute.

### Section 3 - Accessing and Modifying Values

Once the class is created, class methods can be used to access and modify the dict values. The class methods should use the class attributes to access and modify the dict values.

### Section 4 - Example

For example, given a nested dict:

```
my_dict = {
    'name': 'John',
    'age': 25,
    'address': {
        'street': '123 Main St.',
        'city': 'New York',
        'state': 'NY'
    }
}
```

The class could be created as follows:

```
class MyDict:
    def __init__(self, my_dict):
        self.name = my_dict['name']
        self.age = my_dict['age']
        self.address = my_dict['address']
    
    def get_name(self):
        return self.name
    
    def set_name(self, name):
        self.name = name
    
    def get_address(self):
        return self.address
    
    def set_address(self, address):
        self.address = address
```

The class methods can then be used to access and modify the dict values. For example, `my_dict_obj.get_name()` will return the name of the person and `my_dict_obj.set_name('Jane')` will set the name to 'Jane'.

---
title: What is the process of dynamically adding a property to a class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can add a property to a class dynamically in Python using the `property()` function.
---

**Contents**

[TOC]

Section 1: Introduction to dynamically adding properties to a class
Python allows us to dynamically add properties to a class at runtime. This can be useful when we want to add properties to a class that we did not expect at the time of writing the code. In this guide, we will see how we can add properties to a class dynamically.

Section 2: Using the setattr() function
We can use the setattr() function to add properties to a class dynamically. The setattr() function takes three arguments: the object to which we want to add the property, the name of the property, and the value of the property.

Here's an example of how we can use the setattr() function to dynamically add a property to a class:

```
class Person:
    pass

person = Person()
setattr(person, 'name', 'John')
print(person.name) # Output: John
```

In this example, we created a class called Person, created an instance of the class, and then used the setattr() function to add a property called name to the instance.

Section 3: Using the __setattr__() function
We can also add properties to a class dynamically by defining the __setattr__() function. The __setattr__() function is a special method in Python that is called when we try to set an attribute of an object. By defining this method in our class, we can perform custom operations on the attribute before it is set.

Here's an example of how we can use the __setattr__() function to dynamically add a property to a class:

```
class Person:
    def __setattr__(self, name, value):
        self.__dict__[name] = value

person = Person()
person.name = "John"
print(person.name) # Output: John
```

In this example, we defined the __setattr__() method in our class and used it to set the value of the property. We accessed the dictionary __dict__ of the instance to set the property.

Section 4: Conclusion
In this guide, we saw how we can add properties to a class dynamically. We can use the setattr() function to add properties to an instance at runtime, or define the __setattr__() function to define custom operations when setting a property. These techniques allow us to add properties to a class as needed without modifying the class definition.

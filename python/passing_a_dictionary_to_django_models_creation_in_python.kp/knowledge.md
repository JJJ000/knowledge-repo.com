---
title: Is it possible to pass a dictionary to django models during creation?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: No, a dictionary cannot be passed directly to Django models on create, instead, keyword arguments should be passed.
---

**Contents**

[TOC]

Yes, a dictionary can be passed to Django models on create in Python. This can be done in several ways. 

**Using the `**` operator**

One way to pass a dictionary to Django models on create is to use the `**` operator, which allows a dictionary's key-value pairs to be passed as keyword arguments to a function. Here's an example:

```
data = {'name': 'John Doe', 'age': 25, 'email': 'johndoe@example.com'}
person = Person.objects.create(**data)
```

In this example, a dictionary named `data` is defined with three key-value pairs. The `create` method of the `Person` model is then called, with the `**data` argument passed to it. This will create a new `Person` object with the attributes specified in the dictionary.

**Using the object's `__dict__` attribute**

Another way to pass a dictionary to Django models on create is to use the object's `__dict__` attribute. Here's an example:

```
data = {'name': 'John Doe', 'age': 25, 'email': 'johndoe@example.com'}
person = Person(**data)
person.save()
```

In this example, a dictionary named `data` is defined with three key-value pairs. An instance of the `Person` model is then created, with the dictionary's key-value pairs passed to it as arguments using the `**` operator. Finally, the `save` method is called on the instance to save it to the database.

**Using the `fields` argument**

A third way to pass a dictionary to Django models on create is to use the `fields` argument of the `create` method. Here's an example:

```
data = {'name': 'John Doe', 'age': 25, 'email': 'johndoe@example.com'}
person = Person.objects.create(fields=data)
```

In this example, a dictionary named `data` is defined with three key-value pairs. The `create` method of the `Person` model is then called, with the `fields=data` argument passed to it. This tells Django to use the key-value pairs of the dictionary as the field names and values for the new object.

**Using the `from_db_value` method**

Another way to pass a dictionary to Django models on create is to define a custom field that can be constructed from a dictionary. This can be done by defining a custom field that overrides the `from_db_value` method. Here's an example:

```
class CustomDictField(models.TextField):
    def from_db_value(self, value, expression, connection):
        if value is None:
            return None
        return json.loads(value)
```

In this example, a `CustomDictField` class is defined that inherits from Django's `TextField`. The `from_db_value` method is overridden to return a dictionary object constructed from the JSON string stored in the database. Once this field is defined, it can be used in a model to create a new object from a dictionary:

```
data = {'name': 'John Doe', 'age': 25, 'email': 'johndoe@example.com'}
person = Person.objects.create(data=data)
```

In this example, a dictionary named `data` is defined with three key-value pairs. The `create` method of the `Person` model is then called, with the `data=data` argument passed to it. This tells Django to use the dictionary as the value for the `data` field, which is defined as a `CustomDictField`. The `from_db_value` method of the `CustomDictField` is then called to convert the value back into a dictionary object.

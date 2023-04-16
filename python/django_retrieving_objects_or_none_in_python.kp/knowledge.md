---
title: What is the best way to retrieve an object from django if it exists, or return none if it does not?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the get() method on the queryset to retrieve the object or None if it does not exist.
---

**Contents**

[TOC]

## Using get()

The `get()` method of the queryset object can be used to retrieve an object from the database if it exists, or `None` if it does not exist. It takes two arguments: the first is a dictionary containing the field names and values to search for, and the second is an optional boolean indicating whether to raise an exception if the object does not exist.

For example, if we have a model called `Person` with a field called `name` and we want to retrieve a person with the name "John", we can use the following code:

```python
person = Person.objects.get(name='John')
```

If an object with the name "John" exists in the database, it will be returned. If not, `None` will be returned.

## Using filter()

The `filter()` method of the queryset object can also be used to retrieve an object from the database if it exists, or `None` if it does not exist. It takes a dictionary containing the field names and values to search for, and returns a queryset containing all objects that match the criteria.

For example, if we have a model called `Person` with a field called `name` and we want to retrieve a person with the name "John", we can use the following code:

```python
person = Person.objects.filter(name='John').first()
```

If an object with the name "John" exists in the database, it will be returned. If not, `None` will be returned.

## Using get_or_create()

The `get_or_create()` method of the queryset object can also be used to retrieve an object from the database if it exists, or create it if it does not exist. It takes two arguments: the first is a dictionary containing the field names and values to search for, and the second is an optional dictionary containing the field names and values to use when creating the object.

For example, if we have a model called `Person` with a field called `name` and we want to retrieve a person with the name "John" or create one if it does not exist, we can use the following code:

```python
person, created = Person.objects.get_or_create(name='John')
```

If an object with the name "John" exists in the database, it will be returned. If not, a new object will be created with the name "John" and returned.

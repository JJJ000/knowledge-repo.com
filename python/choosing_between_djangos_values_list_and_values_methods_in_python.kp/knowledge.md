---
title: What is the difference between using values_list and values in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Django values\_list returns a list of tuples containing requested field values from queryset, whereas values returns a QuerySet that returns dictionaries, where each dictionary represents an object, with keys being the object field names.
---

**Contents**

[TOC]

Introduction
------------

Django values_list and values are two methods that can be used to retrieve data from a database using Django. While both methods are similar, they have some key differences that are important to understand before deciding which one to use.

What is values_list?
---------------------

values_list is a Django method that returns a QuerySet containing tuples of values instead of objects. You can think of it as a list of dictionaries, where each dictionary represents a single database row. The keys in the dictionary are the field names, and the values are the values of those fields.

For example, if you have a model called "Person" with fields "name" and "age", and you call values_list("name", "age"), you'll get back something like this:

    [("John", 30), ("Jane", 25), ("Bob", 40)]

What is values?
---------------

values is another Django method that can be used to retrieve data from a database. Unlike values_list, it returns a QuerySet containing dictionaries instead of tuples. Each dictionary represents a single database row, and the keys in the dictionary are the field names.

For example, if you have the same "Person" model as before and you call values("name", "age"), you'll get back something like this:

    [{"name": "John", "age": 30}, {"name": "Jane", "age": 25}, {"name": "Bob", "age": 40}]

Values vs values_list: Which one to use?
----------------------------------------

The choice between values and values_list depends on your specific use case. Here are some factors to consider:

- Use values_list if you only need to retrieve specific fields from the database and you don't need to work with objects.
- Use values if you want to retrieve specific fields from the database and you want to work with dictionaries that represent database rows.
- Use the regular query syntax (i.e. not values or values_list) if you need to retrieve entire objects from the database.
- Use values_list over values if you're concerned about performance. Because values_list returns tuples instead of dictionaries, it can be faster (especially for large QuerySets). However, values_list can be less readable than values because you have to remember the order of the fields.

Conclusion
----------

Values and values_list are both useful methods that can be used to retrieve data from a database in Django. The choice between them depends on your specific use case and whether you need to work with objects or dictionaries. Keep in mind that there are performance trade-offs between the two methods, so choose the one that best fits your needs.

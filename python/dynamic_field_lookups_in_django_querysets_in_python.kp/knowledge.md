---
title: How can a queryset be filtered with dynamic field lookups in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can use the double-underscore syntax `\_\_` in your filter argument to reference a field on a related model or to perform lookups, such as `Model.objects.filter(field1\_\_icontains=`search\_term`)`.
---

**Contents**

[TOC]

# Introduction

Django is a very popular Python-based web framework that provides a powerful tool for querying databases using its ORM. One of the key features of Django's ORM is the ability to filter QuerySets using dynamic field lookups. This means that the fields used to filter a queryset can be dynamic and determined at runtime, allowing for greater flexibility in querying models. In this article, we will explore how to filter a QuerySet with dynamic field lookups in Python.

# Setting up Models

Before we dive into dynamic field lookups, we need to set up some models to work with. For simplicity, we will create a simple model with two fields - `name` and `age`.

```python
from django.db import models

class Person(models.Model):
    name = models.CharField(max_length=100)
    age = models.IntegerField()
```

# Static field lookups

Before we get to dynamic field lookups, let's first look at static field lookups. Static field lookups allow us to filter a QuerySet using a fixed set of fields, and Django provides a number of built-in field lookups that we can use. For example, if we want to filter all people with the name "John", we can use the `__exact` lookup:

```python
Person.objects.filter(name__exact='John')
```

Similarly, if we want to filter all people whose age is greater than or equal to 18, we can use the `__gte` lookup:

```python
Person.objects.filter(age__gte=18)
```

# Dynamic field lookups

Static field lookups are great, but sometimes we need to filter models based on user input, which means that the fields used to filter a queryset may not be known in advance. This is where dynamic field lookups come in.

Dynamic field lookups allow us to construct filters using fields that are determined at runtime. One way to do this is to use the `**` syntax to pass a dictionary of filters to the `filter` method. For example, if we have a dictionary of filters like this:

```python
filters = {'name__exact': 'John', 'age__gte': 18}
```

We can construct a filter by unpacking the dictionary using the `**` syntax:

```python
Person.objects.filter(**filters)
```

This is equivalent to:

```python
Person.objects.filter(name__exact='John', age__gte=18)
```

Another way to construct dynamic filters is to use the `Q` object. The `Q` object allows us to construct complex filters by combining multiple lookups using logical operators like `|` (OR) and `&` (AND). For example, if we want to filter all people whose name is "John" or age is greater than or equal to 18, we can use the following code:

```python
from django.db.models import Q

Person.objects.filter(Q(name='John') | Q(age__gte=18))
```

In this example, we have used the `Q` object to construct a filter that matches people with either `name` equal to "John" OR `age` greater than or equal to 18.

# Conclusion

In this article, we have explored how to filter a QuerySet with dynamic field lookups in Python. We have seen that Django provides a number of ways to construct dynamic filters, including using the `**` syntax to unpack a dictionary of filters and using the `Q` object to construct complex filters. When filtering models based on user input, dynamic field lookups can be a powerful tool to provide greater flexibility and expressive power in querying models.

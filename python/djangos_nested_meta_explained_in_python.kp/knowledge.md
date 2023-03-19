---
title: Could you describe the functioning of django's meta class when it is nested?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Django`s nested Meta class allows developers to define metadata for a model within the model class itself.
---

**Contents**

[TOC]

## Introduction 

Django's nested Meta class is a class that is used to define metadata for a model class. This metadata can be used to define various attributes of the model such as ordering, permissions, and database settings. 

In this article, we will discuss how Django's nested Meta class works in Python. 

## Creating a Django Model 

To understand how the nested Meta class works, let's first create a simple Django model: 

```python 
from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.CharField(max_length=50)
    published_date = models.DateField()
```

This model has three fields: title, author, and published_date. 

## Defining Metadata with the Meta Class 

To define metadata for this model, we can use the nested Meta class. Let's define some metadata for this model: 

```python
class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.CharField(max_length=50)
    published_date = models.DateField()

    class Meta:
        ordering = ['-published_date']
```

In this example, we have added a nested Meta class to our Book model. Within this Meta class, we have defined the ordering attribute to sort the results of our queries in reverse chronological order based on the published_date field. 

## Accessing Metadata 

We can access this metadata in several different ways. One way is to use the get_meta() method of a model instance: 

```python 
book = Book(title='The Great Gatsby', author='F. Scott Fitzgerald', published_date='1925-04-10')
meta = book._meta
ordering = meta.ordering
```

In this example, we create a new Book instance and then access its _meta attribute. We can then access the ordering attribute within the Meta class. 

## Overriding Metadata 

We can override the metadata defined in the nested Meta class by creating a subclass and modifying the metadata in that subclass. For example: 

```python 
class ModernBook(Book):
    class Meta:
        ordering = ['published_date']

modern_book = ModernBook(title='The Catcher in the Rye', author='J.D. Salinger', published_date='1951-07-16')
```

In this example, we create a new subclass of our Book model called ModernBook. Within the nested Meta class of the ModernBook model, we override the ordering attribute to sort the results of our queries in chronological order based on the published_date field. 

## Conclusion 

In this article, we discussed how Django's nested Meta class works in Python. We learned how to define metadata for a model using the nested Meta class, how to access that metadata, and how to override the metadata in a subclass. The nested Meta class is a powerful tool for customizing the behavior of Django models.

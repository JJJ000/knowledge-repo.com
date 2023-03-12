---
title: In this django app tutorial, what does the term choice_set mean?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: choice\_set is a reverse relation to the Choice model from the Poll application tutorial allowing to access all the choices for a given Poll instance.
---

**Contents**

[TOC]

## Overview of Django app tutorial

This Django app tutorial is designed to help developers learn how to build a simple web application using Python and Django. The tutorial covers the basics of setting up a Django project, creating a database model, and creating views and templates to display data. The main focus of the tutorial is on creating forms, which allow users to input data into the database.

## What is choice_set?

`choice_set` is a QuerySet-like method in Django that is automatically generated by the framework when a `ForeignKey` field is defined in a model. This method allows you to access the related objects that are associated with the foreign key. The name `choice_set` is derived from the fact that the related objects are typically presented to the user as a set of choices in a form.

## How does choice_set work?

When a `ForeignKey` field is defined in a model, Django creates a hidden attribute on the model class with the name of the field suffixed with `_set`. For example, if you have a `Post` model with a foreign key to a `User` model, Django creates a `user_set` attribute on the `Post` model. This attribute is actually a method that returns a `QuerySet` object representing the related objects.

To use `choice_set`, you simply call the method on the object that has the foreign key. For example, if you have a `Post` object called `my_post`, you can access the related `User` objects like this:

```python
my_post.user_set.all()
```

This will return a `QuerySet` containing all the `User` objects that are related to `my_post`.

## Conclusion

In this tutorial, we have learned about `choice_set`, which is a useful method in Django that allows you to access related objects through a foreign key. This method is automatically generated by Django and is simple to use, making it a powerful and valuable tool for building web applications.
---
title: Make a django model or modify it if it already exists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To create a Django model, use the `Model` class from the `django.db.models` module or to update an existing model, simply modify the model class and generate new migrations.
---

**Contents**

[TOC]

# Introduction

Django is a high-level web framework written in Python that makes it easy to create web applications. One of the core components of Django is its object-relational mapping (ORM) system. The ORM system allows developers to create models in Python that map to database tables, which makes it easy to perform database operations without having to write raw SQL queries.

In this article, we will discuss how to create a Django model, as well as how to update an existing model.


## Creating a Django Model

To create a Django model, we need to define a subclass of the `django.db.models.Model` class. Each attribute of the model class represents a field in the corresponding database table. For example, the following model defines a table that stores information about books:

``` python
from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.CharField(max_length=100)
    publication_date = models.DateField()
```

In this example, the `Book` model has three fields: `title`, `author`, and `publication_date`. The `CharField` and `DateField` classes represent string and date fields, respectively.

Once we have defined our model, we need to create a migration that will apply the changes to the database schema. To create a migration, we can run the following command:

``` python
python manage.py makemigrations
```

This will generate a migration file that we can then apply to the database using the `migrate` command:

``` python
python manage.py migrate
```

Now that our model and migration have been created, we can use the model to perform database operations.


## Updating a Django Model

To update an existing Django model, we can simply modify the model class and create a new migration. For example, suppose we want to add a new field called `publisher` to our `Book` model:

``` python
from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.CharField(max_length=100)
    publication_date = models.DateField()
    publisher = models.CharField(max_length=100)
```

After modifying our model, we can create a new migration using the `makemigrations` command:

``` python
python manage.py makemigrations
```

This will generate a new migration file that contains the changes we made to the `Book` model. We can then apply the migration using the `migrate` command:

``` python
python manage.py migrate
```

And that's it! Our `Book` model now has a new field called `publisher`, and all existing data in the `Book` table is preserved.

## Conclusion

Django makes it easy to create models that map to database tables, and to update them as our application evolves. By defining a Python class that subclasses `django.db.models.Model`, we can define the fields of our model and use the ORM system to perform database operations. Updating a model is just a matter of modifying the Python class and generating a new migration. With Django's powerful ORM system, we can focus on building our application's logic instead of worrying about low-level database operations.

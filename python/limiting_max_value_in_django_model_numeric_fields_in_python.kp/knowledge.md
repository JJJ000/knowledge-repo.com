---
title: What is the process to set a maximum value for a numeric field in a django model?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `validators` parameter in the field definition to add a MaxValueValidator with the desired maximum value.
---

**Contents**

[TOC]

## Section 1: Introduction to Django Models

Django is a web framework for Python which provides a Model-View-Controller (MVC) architecture. Django Models are an important part of this architecture, which define the structure of the database tables to be used in the application. Django Models are written in Python and define the fields and types that will be used in the database tables. 

## Section 2: Defining a Numeric Field in a Django Model

In order to limit the maximum value of a numeric field in a Django Model, we first need to define the field. Numeric fields in Django are represented by the `IntegerField` and `DecimalField` classes. For example, to define an `IntegerField` for a Django Model, we can write:

```python
from django.db import models

class MyModel(models.Model):
    my_integer_field = models.IntegerField()
```

Similarly, to define a `DecimalField`, we can write:

```python
from django.db import models

class MyModel(models.Model):
    my_decimal_field = models.DecimalField(max_digits=5, decimal_places=2)
```

In the above example, `max_digits` and `decimal_places` are attributes of the `DecimalField` class, which define the maximum number of digits and decimal places allowed for the field, respectively.

## Section 3: Limiting the Maximum Value of a Numeric Field

Once the numeric field has been defined in the Django Model, we can limit its maximum value using the `validators` argument of the field. The `validators` argument takes a list of validator functions which will be applied to the field value. The `MaxValueValidator` class can be used to limit the maximum value of a numeric field. For example, to limit the `my_integer_field` in the `MyModel` Django Model to a maximum value of 100, we can write:

```python
from django.core.validators import MaxValueValidator

class MyModel(models.Model):
    my_integer_field = models.IntegerField(validators=[MaxValueValidator(100)])
```

Similarly, to limit the `my_decimal_field` in the `MyModel` Django Model to a maximum value of 999.99, we can write:

```python
from django.core.validators import MaxValueValidator

class MyModel(models.Model):
    my_decimal_field = models.DecimalField(max_digits=5, decimal_places=2, validators=[MaxValueValidator(999.99)])
```

## Section 4: Conclusion

In this article, we learned how to limit the maximum value of a numeric field in a Django Model using the `validators` argument and the `MaxValueValidator` class. This is important for ensuring data integrity in the application and preventing invalid data from being stored in the database.

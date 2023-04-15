---
title: What's the reason for django's model.save() not invoking full_clean()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Because model.save() is intended for efficient saving of data, while full\_clean() is intended for data validation and cleaning.
---

**Contents**

[TOC]

## Background 

Django is a powerful web framework written in Python that follows the model-view-controller (MVC) architecture. One of the core concepts in Django is `models`, which are Python classes that define the structure and behavior of a database table. Django provides a convenience method called `model.save()` to save the data of a model object to the database, which can be called from within a Django view or model's method. However, it does not call the `full_clean()` method by default, which is a validation method provided by Django. This article explains why `model.save()` doesn't call `full_clean()` method and how to resolve the issue.

## Why Doesn't `model.save()` Call `full_clean()` Method by Default?

The `model.save()` method does not call the `full_clean()` validation method by default. This can lead to the undesirable scenario where invalid data is stored in the database, which can cause bugs and security issues. However, there are several reasons why `model.save()` does not call `full_clean()` by default:

1. Performance: If Django called `full_clean()` on every `model.save()` operation, it could result in a significant performance hit, especially for complex models with many fields and validations.

2. Flexibility: Django provides developers with the flexibility to choose when and how to validate the data using `full_clean()`. For example, a developer might want to perform custom validation on a specific field or set of fields, which can be done using `full_clean()`.

3. Historically: The `model.save()` method predates the `full_clean()` method, and calling `full_clean()` on every `model.save()` would have been too disruptive to the existing codebase.

## How to Call `full_clean()` Method from `model.save()`?

In Django, it is possible to call the `full_clean()` method from within the `model.save()` method manually. This can be done by overriding the `save()` method of the model and calling `full_clean()` before super().save() method.

```python
from django.db import models

class MyModel(models.Model):
    name = models.CharField(max_length=100)
    age = models.IntegerField()

    def save(self, *args, **kwargs):
        self.full_clean()
        super().save(*args, **kwargs)

```

In this example, the `MyModel.save()` method is overridden to call `full_clean()` before calling the parent `save()` method. Now every time `MyModel.save()` method is called, it will first validate the data using `full_clean()` before saving it.

## Conclusion

In conclusion, `model.save()` does not call `full_clean()` by default due to performance and flexibility reasons. However, it is possible to call `full_clean()` manually from within `model.save()` by overriding the method. This ensures that the data being saved to the database is valid and reduces the likelihood of bugs and security issues.

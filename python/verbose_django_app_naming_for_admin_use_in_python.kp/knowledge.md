---
title: Could you provide a verbose name for a django application to be utilized across the admin interface?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Yes, by setting the verbose\_name attribute in the app`s AppConfig class.
---

**Contents**

[TOC]

# Introduction

Yes, we can give a Django app a verbose name for use throughout the admin in Python. In this tutorial, we will learn how to specify a verbose name for a Django app using different methods.

## 1. Using the `verbose_name` attribute in `AppConfig` class

```python
from django.apps import AppConfig


class MyAppConfig(AppConfig):
    name = 'myapp'
    verbose_name = 'My App'
```

In the above code snippet, we are creating an `AppConfig` class for our Django app `myapp`. We are specifying the `verbose_name` attribute with a friendly name "My App". This name will be used throughout the admin to refer to our app. We can use this `My App` instead of `myapp`. 

We need to register the `MyAppConfig` class in our `settings.py` file as follows:

```python
...
INSTALLED_APPS = [
    'myapp.apps.MyAppConfig',
    ...
]
...
```

## 2. Using the `Meta` class in `models.py` file

```python
from django.db import models


class MyModel(models.Model):
    # fields

    class Meta:
        verbose_name_plural = 'My Models'
        verbose_name = 'My Model'
```

In the above code snippet, we are defining our model `MyModel` and specifying the `Meta` class to assign a verbose name for our model. We are using the `verbose_name_plural` attribute to give the plural name of our model as `My Models` and the `verbose_name` attribute to give a singular name as `My Model`. This name will be used throughout the admin to refer to our model.

## 3. Using the `label` attribute in `ModelForm` class

```python
from django import forms
from .models import MyModel


class MyModelForm(forms.ModelForm):
    class Meta:
        model = MyModel
        fields = '__all__'
        labels = {
            'name': 'My Field Name'
        }
```

In the above code snippet, we are creating a `ModelForm` class for our model `MyModel`. We are defining the `labels` attribute to give a verbose name to our field `name`. This name will be used throughout the admin to refer to our field instead of `name`.

## 4. Using the `verbose_name` attribute in `ForeignKey` and `ManyToManyField` fields

```python
from django.db import models


class MyRelatedModel(models.Model):
    # fields

    class Meta:
        verbose_name_plural = 'My Related Models'
        verbose_name = 'My Related Model'


class MyModel(models.Model):
    related_model = models.ForeignKey(MyRelatedModel, verbose_name='My Related Model', on_delete=models.CASCADE)
    many_to_many = models.ManyToManyField(MyRelatedModel, verbose_name='My Related Models')

    class Meta:
        verbose_name_plural = 'My Models'
        verbose_name = 'My Model'
```

In the above code snippet, we are defining two fields `related_model` and `many_to_many` in our model `MyModel`. We are specifying the `verbose_name` attribute for both fields to give names in the admin interface. We are referring to the `MyRelatedModel` model and specifying its verbose name as `My Related Model` and `My Related Models`. These names will be used throughout the admin to refer to the `ForeignKey` and `ManyToManyField` fields.

# Conclusion

In this tutorial, we have learned how to specify verbose names for a Django app, model, form and fields using different methods. This helps users to identify the app, model, form and fields easily in the admin interface.

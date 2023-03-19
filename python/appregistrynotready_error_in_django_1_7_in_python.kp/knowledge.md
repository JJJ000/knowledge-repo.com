---
title: The error message 'models aren't loaded yet' is thrown by django 1.7 indicating an issue with django.core.exceptions.appregistrynotready
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The error occurs when trying to access the models before the Django application registry has been fully initialized.
---

**Contents**

[TOC]

# Introduction

Django is a popular web framework written in Python that allows developers to build high-quality web applications quickly and easily. However, sometimes you may run into issues with the framework, such as the "django.core.exceptions.AppRegistryNotReady: Models aren't loaded yet" error. In this article, we will explore this error in more detail and provide solutions to fix it.

# Understanding the Error

The "django.core.exceptions.AppRegistryNotReady: Models aren't loaded yet" error usually occurs when you try to reference a Django model before it has been loaded. This can happen in several scenarios, such as importing a model in your settings.py file or in your app's __init__.py file.

When Django starts up, it needs to load all of the models that are defined in your apps. If it encounters an error while trying to load a model, it can't continue and will throw the "AppRegistryNotReady" error.

# Solutions

There are a few solutions to the "django.core.exceptions.AppRegistryNotReady: Models aren't loaded yet" error, depending on where and why it is happening in your code.

## Solution 1: Move imports

If you are importing a model in your settings.py file or in your app's __init__.py file, try moving the import to a later point in your code. For example, if you are importing a model in your app's __init__.py file, you could move the import inside a function that is called later in your code.

## Solution 2: Use AppConfig.ready()

Another solution is to use the AppConfig.ready() method to delay the use of the models until they have been fully loaded. This method is called when the app is ready to use, and you can use it to perform any actions that depend on the models being loaded. Here's an example:

```python
from django.apps import AppConfig

class MyAppConfig(AppConfig):
    name = 'myapp'

    def ready(self):
        # Import your models here
        from myapp.models import MyModel
```

## Solution 3: Use signals

Finally, you can use Django signals to execute code only after the models are fully loaded. For example, you could use the post_migrate signal to execute code after all of the migrations have been applied to the database. Here's an example:

```python
from django.db.models.signals import post_migrate
from django.dispatch import receiver

@receiver(post_migrate)
def my_callback(sender, **kwargs):
    # Import your models here
    from myapp.models import MyModel
```

# Conclusion

The "django.core.exceptions.AppRegistryNotReady: Models aren't loaded yet" error can be frustrating, but it is usually easy to fix. By understanding why the error occurs and using the appropriate solution for your code, you can quickly get back to developing your Django web application.

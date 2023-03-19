---
title: The django model does not specify a particular app_label
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: A Django model must include an `app\_label` attribute to specify which app the model belongs to.
---

**Contents**

[TOC]

## Understanding the Error Message

When using Django Models in a project, it's possible to encounter the following error message: "django.core.exceptions.ImproperlyConfigured: Creating a ModelForm without either the 'fields' attribute or the 'exclude' attribute is prohibited; form GuestForm needs updating. Additionally, AddBook doesn't declare an explicit app_label and isn't in an application in INSTALLED_APPS." This error message indicates that there is a problem with the configuration of the model, and specifically that the model doesn't have an explicit app_label declared.

## What is an App in Django?

In Django, an App is a web application that can be installed and reused within different projects. An App usually contains models, views, templates, and other resources that define the behavior and appearance of the application. To create a new App in Django, you can use the `startapp` command, which will create a new directory with the necessary files and configuration.

## Why is an explicit app_label needed?

When creating a model in Django, it's necessary to specify an app_label, which is the name of the application that the model belongs to. This is important because Django uses the app_label to organize and reference the models across different parts of the framework, such as the admin interface, database migrations, and queries. If a model doesn't have an explicit app_label declared, Django may not be able to find and use it correctly.

## How to fix the error message?

To fix the "doesn't declare an explicit app_label" error message in Django, you need to add an `app_label` attribute to the model's Meta class, like this:

```python
class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.CharField(max_length=100)
    # other fields

    class Meta:
        app_label = 'myapp' # replace with your app name
```

Make sure to replace the `myapp` string with the name of your application. Once you have added the `app_label`, you should be able to use the model without encountering the error message. If you have multiple models in your application, you will need to add the `app_label` attribute to each one of them. Also, make sure that the application is included in the `INSTALLED_APPS` list in the project's settings file.

---
title: Modify the text in 'django administration' header of django admin
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To change the header `Django administration` text in Python, override the `AdminSite.site\_header` attribute.
---

**Contents**

[TOC]

## Get familiar with Django admin customization

Django provides a built-in admin interface to manage the application's data. It is a powerful tool that allows developers to create, read, update and delete (CRUD) the app's data.

However, by default, Django admin presents a generic look and feel. The header text - 'Django administration' - is one of the identifying features.

It is possible to change the header text from the default to something more specific to our application. In this tutorial, we will explain how to achieve this in Python.

## Modify the header text

To change the header text, navigate to the admin.py file and import the admin module from django.contrib.

```python
from django.contrib import admin
```

Next, override the AdminSite class from django.contrib.admin.sites. This class defines a site-wide admin interface that permits alteration of the look and feel of the admin pages.

```python
class CustomAdminSite(admin.AdminSite):
    site_header = "Your Custom Header Text"
```

In the CustomAdminSite class above, the site_header attribute is set to the desired header text.

## Register your models with your custom admin site

After customizing the admin interface, we need to replace the default Django admin with the custom one. In this example, we will change the admin interface to the custom one by registering the models in our application:

```python
from django.contrib.admin import register
from django.contrib.auth.models import User

register(User, site=CustomAdminSite)
```

In the above code snippet, we first import Django User from django.contrib.auth.models module. Next, using the `register()` decorator, we register our User model with our custom admin site.

## Conclusion

In this article, we have seen how to customize the header text in Django admin from the default 'Django administration' text to our custom text. We learned how to override the AdminSite class and register our models with the custom admin site.

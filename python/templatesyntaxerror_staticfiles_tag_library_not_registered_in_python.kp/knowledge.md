---
title: The tag library 'staticfiles' has not been registered - this is causing a templatesyntaxerror in django
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Make sure to add `django.contrib.staticfiles` to your INSTALLED\_APPS list in settings.py.
---

**Contents**

[TOC]

## Overview
When working with Django, you may encounter a TemplateSyntaxError that says "'staticfiles' is not a registered tag library." This error occurs when Django cannot find and load the staticfiles module, which is responsible for handling static files in your Django project.

## Check Staticfiles App is Installed
The first thing to check is that the staticfiles app is installed in your Django project. You can do this by opening the INSTALLED_APPS list in your project's settings.py file and making sure that 'django.contrib.staticfiles' is included. If it isn't, add it to the list and save the file.

## Check Template Tags are Included
The next thing to check is that you have included the staticfiles template tags in your template. You can do this by adding the following line at the top of your template:

```
{% load staticfiles %}
```

This line tells Django to load the staticfiles tag library, which includes the template tags you need to work with static files. Make sure this line is included in all of your templates that use static files.

## Run Collectstatic Command
If you have checked that the staticfiles app is installed and the template tags are included, but you still receive the TemplateSyntaxError, it may be that Django has not yet collected your static files. You can do this by running the following command from the command line:

```
python manage.py collectstatic
```

This will collect all of your static files and place them in the specified STATIC_ROOT directory. Once this command has completed, try running your Django project again and see if the TemplateSyntaxError has been resolved.

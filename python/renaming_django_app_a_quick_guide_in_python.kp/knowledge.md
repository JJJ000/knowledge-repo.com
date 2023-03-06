---
title: How can the name of a django application be modified?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To change the name of a Django app in Python, simply rename the app directory and update the app name in the app config file.
---

**Contents**

[TOC]

# Introduction

In Django, changing the name of an app can be a bit of work because it involves renaming files, updating references, and making sure that everything still works correctly. This guide will walk you through the process of changing the name of a Django app, step by step.

# Step 1 - Rename the app directory

The first step in changing the name of a Django app is to rename its directory. This can be done using your file explorer or command line interface (CLI).

Here is an example of how to rename an app called "myapp" to "newapp" using the terminal:

```bash
cd /path/to/myproject/
mv myapp newapp
```
# Step 2 - Update references to the app

Once you have renamed the directory, you will need to update any references to the old app name in your project's files. This includes:

- `<app_name>` references in `INSTALLED_APPS` in settings.py
- `urlpatterns` in urls.py
- References to app models in other app's ForeignKey fields or related_names property
- References to the old app name in templates and views

You can use any IDE or text editor you prefer to do this. It is important to do a "Find and Replace" so you don't miss any references.

# Step 3 - Change the app label and name

To properly reflect the name change in Django's admin interface, you will need to update the app label and name in the `apps.py` file:

```python
from django.apps import AppConfig

class NewAppConfig(AppConfig):
    name = 'newapp'
    verbose_name = 'New App'
```

# Step 4 - Make migrations and migrate

After completing the above steps, it is important to create and run a migration to ensure the changes are properly implemented in the database:

```bash
python manage.py makemigrations
python manage.py migrate
```

That's it! With these four steps, you should now have successfully changed the name of your Django app.

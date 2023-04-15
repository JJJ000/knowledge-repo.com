---
title: The makemigrations command in django 1.7 is failing to detect any changes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Make sure that your app is included in the INSTALLED\_APPS list in settings.py or run makemigrations command with the name of the app where you made the changes.
---

**Contents**

[TOC]

## Introduction
Django 1.7 introduced the `makemigrations` command to automatically create migrations based on changes made to models. However, sometimes `makemigrations` may not detect changes made to Python files. In this article, we will explore some possible reasons for this issue and their solutions.

## Missing dependencies
Django's migrations framework relies on the `django.db.migrations` package that has several dependencies. If any of these dependencies are missing, `makemigrations` may not be able to detect changes to models. 

One solution is to install Django and all its dependencies using the `pip` package manager. You can do this by running the following command:
```
pip install -r requirements.txt
```
Another solution is to manually install the missing dependencies using `pip`. For example, if the `MySQLdb` dependency is missing, you can install it using the following command:
```
pip install mysqlclient
```

## Improperly configured settings
Django's migrations framework also depends on the project's settings. If the project's settings are improperly configured or incomplete, `makemigrations` may not be able to detect changes to models.

To fix this issue, ensure that your project's `settings.py` file has the following configuration:
```python
INSTALLED_APPS = [
    # ...other apps
    'django.contrib.contenttypes',
    'django.contrib.auth',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

## Improperly defined models
If the models are not defined correctly, `makemigrations` may not be able to detect changes. This can happen if the models are not defined in a file named `models.py`, or if the models have incorrect syntax.

To fix this issue, ensure that:
- Your models are defined in a file named `models.py` inside the relevant Django app.
- Your models follow the correct syntax.

## Conclusion
In summary, `makemigrations` may fail to detect changes to models due to missing dependencies, improperly configured settings, or improperly defined models. By addressing these issues, you can ensure that `makemigrations` works as expected.

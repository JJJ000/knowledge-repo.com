---
title: What steps should I take to activate cors on django rest framework?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Add `django-cors-headers` to INSTALLED\_APPS in settings.py and add `corsheaders.middleware.CorsMiddleware` and `corsheaders` to MIDDLEWARE in settings.py.
---

**Contents**

[TOC]

## Introduction

Cross-Origin Resource Sharing (CORS) is a security feature that restricts a web page or a web application from requesting data from a different domain or from another server. However, it can sometimes be beneficial to allow CORS, especially for developing applications that require data from different sources.

In this tutorial, we will look at how to enable CORS on Django REST Framework in Python.

## Step 1 — Installing Django CORS headers

The Django CORS headers package can be installed using pip. To do that, open the terminal and type:

```bash
pip install django-cors-headers
```

## Step 2 — Adding Django CORS headers to Django

To add Django CORS headers to Django, add 'corsheaders' to INSTALLED_APPS in your settings.py file, as shown below:

```python
INSTALLED_APPS = [
    ...,
    'corsheaders',
]
```

Then, add 'corsheaders.middleware.CorsMiddleware' to the MIDDLEWARE setting:

```python
MIDDLEWARE = [
    ...,
    'corsheaders.middleware.CorsMiddleware',
    'django.middleware.common.CommonMiddleware',
    ...
]
```

## Step 3 — Configuring Django CORS headers

To configure Django REST Framework to allow CORS for all domains, add the following setting to your settings.py file:

```python
CORS_ORIGIN_ALLOW_ALL = True
```

If you want to allow CORS for specific domains, you can use the CORS_ORIGIN_WHITELIST setting like this:

```python
CORS_ORIGIN_WHITELIST = [
    'http://localhost:3000',
    'http://127.0.0.1:3000',
]
```

## Step 4 — Testing CORS settings

Finally, start your Django development server and test your CORS settings by sending requests from your front-end application or any client application that consumes your server. You should be able to receive data from your server without any CORS errors.

Conclusion

In this tutorial, we have covered how to enable CORS on Django REST Framework in Python using the Django CORS headers package. By following these steps, you can configure your Django project to allow requests from all domains or specific whitelisted domains.

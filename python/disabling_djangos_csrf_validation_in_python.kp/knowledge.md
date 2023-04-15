---
title: Can you provide steps for turning off django's csrf validation?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add @csrf\_exempt decorator to the view function.
---

**Contents**

[TOC]

## Introduction

Cross-Site Request Forgery (CSRF) is a common attack vector on the web that tricks users into performing actions on a website without their consent. Django, being a popular web framework, comes with built-in CSRF protection to prevent such attacks. 

However, there may be situations where you might want to disable the CSRF validation. This might include use cases like developing APIs or building a single-page application (SPA). In this tutorial, we will explore how to disable Django's CSRF validation.

## How to disable CSRF in Django

Disabling CSRF in Django involves making changes to the settings.py file. Follow these steps to disable CSRF in Django:

### Step 1: Locate the settings.py file

The settings.py file is located in the root folder of your Django project.

### Step 2: Add the CSRF middleware class to the MIDDLEWARE setting

Open the settings.py file and locate the MIDDLEWARE setting. By default, this setting contains a list of middleware classes that are applied to all requests/response. Add the following line of code to the MIDDLEWARE setting:

```python
MIDDLEWARE = [
    # ... other middleware classes ...
    'django.middleware.csrf.CsrfViewMiddleware',
    # ... other middleware classes ...
]
```

This middleware class is responsible for enforcing CSRF validation in Django. By adding it to the MIDDLEWARE setting, we can disable the built-in CSRF validation.

### Step 3: Add CSRF_EXEMPT setting

Django allows us to exempt certain views from CSRF validation. We can specify a list of view functions that do not require CSRF validation by adding the CSRF_EXEMPT setting in the settings.py file. 

Add the following code snippet to the settings.py file:

```python
CSRF_EXEMPT = [
    'myapp.views.my_view',
]
```

This code exempts the `my_view` function in the `myapp.views` module from CSRF validation.

### Step 4: Add `@csrf_exempt` decorator to specific views

Another way to disable CSRF validation in individual views is to use the `@csrf_exempt` decorator. Add the `@csrf_exempt` decorator to any views that do not require CSRF validation. Example:

```python
from django.views.decorators.csrf import csrf_exempt

@csrf_exempt
def my_view(request):
    # view logic here
```

In the example above, we have exempted the `my_view` function from CSRF validation.

## Conclusion

In this tutorial, we explored how to disable Django's CSRF validation. We can disable CSRF by adding the CSRF middleware class to the MIDDLEWARE setting, exempting specific views from CSRF validation using the CSRF_EXEMPT setting, or using the `@csrf_exempt` decorator to exempt views on a case-by-case basis. It is important to note that disabling CSRF validation should only be done in cases where it is necessary and appropriate, as it can make your application more vulnerable to attacks.

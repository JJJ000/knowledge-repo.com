---
title: How can I run code in django that only executes once during startup?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Add the code to the ready() method in the AppConfig class in the apps.py file of the relevant app.
---

**Contents**

[TOC]

## Introduction

Django is a powerful web framework written in Python that makes it easy to build web applications fast. When working with Django, there may be times when you need to run some code once when the application starts up. In this article, we will look at how to execute code when Django starts up once only in Python.

## Using App Config Ready method

One of the easiest ways to execute code when Django starts up once only is by using the AppConfig ready method. This method is called by Django once the application is ready to be used. To use this method, follow these steps:

1. Open your `apps.py` file in your Django application.
2. Import the AppConfig class from the django.apps module.
3. Subclass your application's AppConfig from the AppConfig class.
4. Override the ready method with your custom code.
5. Register your AppConfig with the INSTALLED_APPS list in your Django application's `settings.py` file.

```
# apps.py

from django.apps import AppConfig

class MyappConfig(AppConfig):
    name = 'myapp'

    def ready(self):
        print("Hello, world! My Django app has started.")
```

## Using a Middleware

Another way to execute code when Django starts up once only is by using a middleware. A middleware is a way to add processing logic to your Django application's request/response processing pipeline. To use this method, follow these steps:

1. Create a middleware class in your Django application's `middleware.py` file.
2. Override the `__init__` method to initialize your custom code.
3. Override the `process_request` method to execute your custom code when the middleware is processed.
4. Add your middleware class to the MIDDLEWARE list in your Django application's `settings.py` file.

```
# middleware.py

class MyMiddleware:
    def __init__(self, get_response):
        self.get_response = get_response
        print("Hello, world! My Django app has started.")

    def process_request(self, request):
        response = self.get_response(request)

        # Process response

        return response
```

## Using Signals

Finally, you can also execute code when Django starts up once only by using signals. Signals are a way for Django applications to notify each other when certain events occur. To use this method, follow these steps:

1. Import the AppConfig class from the django.apps module.
2. Subclass your application's AppConfig from the AppConfig class.
3. Override the ready method with your custom signal code.
4. Define a signal receiver function to execute your custom code when the signal is received.
5. Connect the receiver function to the signal in your application's `apps.py` file.

```
# apps.py

from django.apps import AppConfig
from django.core.signals import request_started

class MyappConfig(AppConfig):
    name = 'myapp'

    def ready(self):
        request_started.connect(self.my_signal_receiver)

    def my_signal_receiver(sender, **kwargs):
        print("Hello, world! My Django app has started.")
```

## Conclusion

In this article, we have looked at three different ways to execute code when Django starts up once only in Python. Each method has its pros and cons, so choose the one that works best for your application's needs. With these methods, you can easily execute custom code when Django starts up, making it easier to build robust and powerful web applications.

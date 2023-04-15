---
title: When utilizing namespace in include(), an improperlyconfigurederror involving app_name arises
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Make sure to include the app\_name argument in your include() function when using namespaces in your URLconf.
---

**Contents**

[TOC]

Section 1: Brief Explanation
---------------------------
When using namespace in the `include()` function in Python's URL routing, an `ImproperlyConfiguredError` can be raised about `app_name`. This error occurs when the namespace is specified, but the `app_name` attribute is missing in the included app's `urls.py` file.

Section 2: Definition of the include() Function
----------------------------------------------
Python provides a `include()` function in the `django.urls` module for URL routing. It takes at least one argument, a module path to the target app's `urls.py` file. The `include()` function is often used to include URLs of another app, such as a third-party app or a nested app.

Section 3: Explanation of the Namespace and app_name Attributes
-------------------------------------------------------------
In Django, a namespace is a way to differentiate URL patterns of multiple apps that have the same URL pattern names. It is defined by adding a `namespace` argument to the `include()` function. The namespace must be unique within the project.
 
On the other hand, the `app_name` attribute is a way to refer to an app's URL pattern names in the project level, which allows the URL pattern names to be namespaced. It must also be unique within the project.

Section 4: Solution to the ImproperlyConfiguredError
---------------------------------------------------
To resolve the `ImproperlyConfiguredError` about `app_name`, make sure the target app's `urls.py` file has the `app_name` attribute defined. This is done by assigning the attribute a string value that represents the app's name. For example, if an app named `blog` has its URL patterns included in another app, then the `blog/urls.py` file must have the following line:

`app_name = 'blog'`

If the `app_name` attribute is missing or not assigned a value, or it conflicts with other app names, the `ImproperlyConfiguredError` will be raised.

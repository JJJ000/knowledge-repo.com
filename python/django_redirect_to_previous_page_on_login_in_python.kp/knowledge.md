---
title: Django directing back to the previous page post login
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use Django`s built-in `next` variable to store the URL of the previous page and redirect to it after the user logs in.
---

**Contents**

[TOC]

Section 1: Introduction

In this tutorial, we will learn how to redirect to the previous page after login in a Django web application using Python. The redirecting to the previous page can help users save time by not having to navigate back to the previous page and continue where they left off.

Section 2: Getting Started

To begin, we first need to install Django using pip. Open the command prompt or terminal and type the following command:

`pip install django`

Next, create a new Django project by typing the following command in your project directory:

`django-admin startproject example_project`

After creating the project, create a new app inside the project using the following command:

`python manage.py startapp accounts`

Next, create the views and templates directory inside the accounts app directory.

Section 3: Implementation

Now, let's implement the code for redirecting to the previous page after login. First, we need to add a login view in the accounts/views.py file.

```python
from django.shortcuts import render, redirect
from django.contrib.auth import authenticate, login

def login_view(request):
    if request.method == 'POST':
        username = request.POST.get('username')
        password = request.POST.get('password')
        user = authenticate(request, username=username, password=password)
        if user is not None:
            login(request, user)
            return redirect(request.META.get('HTTP_REFERER', '/'))
    return render(request, 'accounts/login.html')
```

Here, we have created a function named login_view that takes a request object as an argument. If the request method is POST, we get the username and password from the request object. We then authenticate the user using the authenticate function and login the user by calling the login function. After the user has been logged in, we use the redirect function to redirect the user to the previous page by accessing the HTTP_REFERER value from the request.META dictionary. If the HTTP_REFERER value is not available, we redirect the user to the homepage.

Next, we need to create a login.html template in the accounts/templates/accounts directory. Here is an example of a simple login form that we can use for our example:

```html
{% extends 'base.html' %}

{% block content %}
  <form method="post">{% csrf_token %}
    <label for="username">Username:</label>
    <input type="text" name="username"><br>
    <label for="password">Password:</label>
    <input type="password" name="password"><br>
    <input type="submit" value="Login">
  </form>
{% endblock %}
```

Finally, we need to define a URL pattern for our login_view in the example_project/urls.py file. Here is an example of how to do this:

```python
from django.urls import path
from accounts.views import login_view

urlpatterns = [
    path('login/', login_view, name='login'),
]
```

Section 4: Conclusion

In this tutorial, we have learned how to redirect to the previous page after login in a Django web application using Python. By implementing this feature, we can improve the user experience of our web application by saving the user time and allowing them to continue where they left off.

---
title: Redirecting a page using Python and django
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: In Django, the redirect method in the HttpResponseRedirect class is used to redirect to a different URL or view.
---

**Contents**

[TOC]

Section 1: Introduction to Python + Django Page Redirect

In web development, page redirect is the process of forwarding a user from one webpage URL to another webpage URL. This is usually done to ensure that the user is taken to the correct page after clicking a link or performing a certain action. In Python-based web development using Django, page redirecting can be done in a few simple steps.

Section 2: Using Django's HttpResponseRedirect

Django has a built-in HttpResponseRedirect class that can be used to redirect users from one page to another. To use this class, first import it from the Django HTTP response library using the following statement:

```python
from django.http import HttpResponseRedirect
```

Then, in your view function, you can use the `HttpResponseRedirect` class to perform the redirect. This class accepts a single argument, which is the URL that you want to redirect the user to. Here's an example:

```python
def my_view(request):
    # ... code to process request ...
    return HttpResponseRedirect('/new-page-url/')
```

This will redirect the user to the `new-page-url` page when the `my_view` function is called.

Section 3: Using Django's redirect() function

Django also provides a redirect() function that can be used to perform page redirections. This function is part of the django.shortcuts module and can be used as follows:

```python
from django.shortcuts import redirect

def my_view(request):
    # ... code to process request ...
    return redirect('/new-page-url/')
```

As you can see, this is similar to using the `HttpResponseRedirect` class, but the `redirect()` function can also accept a named URL pattern as its argument. For example:

```python
from django.shortcuts import redirect

def my_view(request):
    # ... code to process request ...
    return redirect('myapp:view-name')
```

This will redirect the user to the view named `view-name` in the `myapp` application.

Section 4: Using Reverse() with redirect()

Finally, Django provides a `reverse()` function that can be used to reverse URL patterns and retrieve their associated URLs. This function can be used in conjunction with the `redirect()` function to perform advanced URL redirections. Here's an example:

```python
from django.shortcuts import redirect, reverse

def my_view(request):
    # ... code to process request ...
    my_url = reverse('myapp:view-name', args=[arg1, arg2])
    return redirect(my_url)
```

This will retrieve the URL associated with the `myapp:view-name` view, passing `arg1` and `arg2` as arguments to the URL pattern. It will then redirect the user to this URL. This approach allows you to decouple your URLs from your views, making your code more flexible and maintainable.

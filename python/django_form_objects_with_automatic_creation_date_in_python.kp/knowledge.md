---
title: The generation of the creation date for django model form objects is done automatically
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Set the model field default parameter to the current date and time using timezone.now() in models.py.
---

**Contents**

[TOC]

## Introduction

Django is a popular web framework in Python that implements the Model-View-Controller (MVC) architecture. It provides a robust and flexible way to create web applications with ease. One of the main features of Django is its built-in support for ModelForms, which allow developers to generate forms based on models automatically. In this article, we'll discuss how to automatically create the creation date for Django model form objects in Python. 

## The Model Definition

Before we can start automatically creating the creation date for model form objects, we need to define our model. For example, let's assume we have a simple model for a blog post:

```
from django.db import models
from django.utils import timezone

class Post(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    created_date = models.DateTimeField(default=timezone.now)
```

In this model definition, we have a `created_date` field that uses the `timezone.now` function as its default value. This means that when a new Post object is created, it will automatically set the `created_date` field to the current time.

## The ModelForm Definition

To create a ModelForm based on our Post model, we can use the built-in `ModelForm` class in Django. Here's an example:

```
from django import forms
from .models import Post

class PostForm(forms.ModelForm):
    class Meta:
        model = Post
        fields = ('title', 'content')
```

In this `PostForm` class, we've specified that we want to use the `Post` model and only include the `title` and `content` fields in the form. However, we haven't included the `created_date` field since we want to automatically set it to the current time.

## Using the ModelForm

Now that we've defined our `Post` model and `PostForm` form, we can use them in a Django view. Here's an example view that creates a new `Post` object using the `PostForm` form:

```
from django.shortcuts import render, redirect
from .forms import PostForm

def create_post(request):
    if request.method == 'POST':
        form = PostForm(request.POST)
        if form.is_valid():
            post = form.save(commit=False)
            post.save()
            return redirect('post_detail', pk=post.pk)
    else:
        form = PostForm()
    return render(request, 'blog/post_edit.html', {'form': form})
```

In this view, we're using the `PostForm` form to create a new `Post` object. When the form is submitted, we're checking if it's valid and then saving it to the database. However, before we save it, we're using Django's `commit=False` option to create a `Post` object but not save it to the database yet. This allows us to set the `created_date` field to the current time before saving it.

```
if form.is_valid():
            post = form.save(commit=False)
            post.created_date = timezone.now()
            post.save()
            return redirect('post_detail', pk=post.pk)
```

## Conclusion

In this article, we've discussed how to automatically create the creation date for Django model form objects in Python. By setting the default value for the `created_date` field in the model definition and using the `commit=False` option in the view, we can set the creation date to the current time before saving the object to the database. This provides a simple and efficient way to add timestamp functionality to Django models.

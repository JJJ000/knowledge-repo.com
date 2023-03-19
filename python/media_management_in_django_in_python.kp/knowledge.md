---
title: Reworded the concepts of media_url and media_root in django
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: MEDIA\_URL and MEDIA\_ROOT are settings in Django used to define the URL and file system path for media files such as images and videos.
---

**Contents**

[TOC]

## Introduction
Django is a web framework for developing applications using the Python programming language. It provides a convenient way to manage static files, such as images, stylesheets, and JavaScript files. In this tutorial, you will learn about MEDIA_URL and MEDIA_ROOT in Django, which are two important settings related to managing static files.

## MEDIA_URL

MEDIA_URL is a setting in Django that specifies the URL path to the directory containing the static files. By default, it is set to "/media/".

```python
# settings.py
MEDIA_URL = '/media/'
```

This means that all files in the media directory will be accessible via URLs starting with "/media/". For example, if you have an image file named "example.jpg" in the media directory, its URL would be "/media/example.jpg". 

You can change this setting to anything you want, depending on your project's needs. Just make sure that the URL path you specify does not conflict with any existing URLs in your application.

## MEDIA_ROOT

MEDIA_ROOT is another setting in Django that specifies the directory on your file system where static files will be stored. By default, it is set to an empty string, which means that Django will look for static files in the directory specified in the STATICFILES_DIRS setting.

```python
# settings.py
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```

This means that all media files uploaded by users will be stored in the "media" directory of your project's root directory. The MEDIA_ROOT setting should always be an absolute path to a directory on your file system.

## Handling User-Generated Content

If your website allows users to upload content, such as images or videos, it's important to handle them properly. Django provides two classes for handling user-generated content: FileField and ImageField.

```python
# models.py
from django.db import models

class User(models.Model):
    username = models.CharField(max_length=30)
    profile_picture = models.ImageField(upload_to='profile_pictures/')
```

The "upload_to" argument specifies the subdirectory within the media directory where the uploaded files will be saved. In this example, all profile pictures will be saved in a subdirectory called "profile_pictures".

When a user uploads a file through a form, Django automatically saves the file in the appropriate directory specified by the "upload_to" argument.

## Conclusion

In this tutorial, you learned about MEDIA_URL and MEDIA_ROOT in Django, which are two important settings related to managing static files. You also learned how to handle user-generated content using the FileField and ImageField classes. By properly configuring these settings and classes, you can ensure that your website's static files are managed and served efficiently.

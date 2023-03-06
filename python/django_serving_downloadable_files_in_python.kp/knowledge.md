---
title: Enabling django to provide files that can be downloaded
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To serve downloadable files in Django, you can use the HttpResponse and FileResponse classes to send the file contents and set appropriate headers.
---

**Contents**

[TOC]

## Setting up media files in Django

To serve downloadable files in Django, we'll need to define a `MEDIA_ROOT` and `MEDIA_URL` in our settings.py file. We'll also need to add some URL patterns to our `urls.py` file to map URLs to file paths.

First, let's make sure we have the necessary settings set up:

```
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
MEDIA_URL = '/media/'
```

Now let's add the necessary URL patterns to our urls.py file:

```
from django.conf import settings
from django.conf.urls.static import static

# ... other URL patterns ...

if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

This will map URLs that start with `/media/` to files that exist in our media root.


## Uploading files to Django

Next, we need to set up a way to upload files to our Django app. One common way to do this is to use Django's built-in `FileField` and `ImageField` models.

Here's an example model that uses both fields:

```
from django.db import models

class MyModel(models.Model):
    name = models.CharField(max_length=100)
    file = models.FileField(upload_to='uploads/')
    image = models.ImageField(upload_to='uploads/')
```

The `upload_to` argument specifies where the file should be saved relative to `MEDIA_ROOT`.

Now we can create a form that allows users to upload files:

```
from django import forms
from .models import MyModel

class MyModelForm(forms.ModelForm):
    class Meta:
        model = MyModel
        fields = ['name', 'file', 'image']
```

We can then use this form in our views to process file uploads.


## Serving downloadable files in Django

Finally, we can serve downloadable files in Django by creating a view that returns a `FileResponse` object.

Here's an example view that serves a file from a file path:

```
from django.http import FileResponse
import os

def download_file(request, file_path):
    file_name = os.path.basename(file_path)
    with open(file_path, 'rb') as fh:
        response = FileResponse(fh, as_attachment=True, filename=file_name)
        return response
```

We can then map a URL pattern to this view:

```
from django.urls import path
from . import views

urlpatterns = [
    # ... other URL patterns ...
    path('download/<str:file_path>', views.download_file),
]
```

Now, when a user visits the `/download/` URL with a file path as a parameter, they will download the file from that path.

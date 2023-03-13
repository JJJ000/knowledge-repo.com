---
title: How can we generate a file and store it in a filefield of a model in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: First, create the file using Python`s built-in open() function, then save it to the model`s FileField using the save() method.
---

**Contents**

[TOC]

Creating a file in Python

To create a file in Python, we can use the built-in `open()` function. Here is an example of creating a text file named `example.txt` and writing some initial content to it:

```python
filename = 'example.txt'
with open(filename, 'w') as file:
    file.write('This is an example file.\n')
    file.write('It was created using Python.\n')
```

The `open()` function takes two required arguments: the filename and the mode in which the file should be opened (such as read-only, write-only, or append). We specify `'w'` for write mode, which will create a new file or overwrite an existing one. The `with` statement ensures that the file is automatically closed when we are done writing to it.

Saving a file to a Django model's FileField

To save a file to a Django model's `FileField`, we first need to create an instance of the model and assign the file to the field. Here is an example using a `Document` model with a `file` field:

```python
from myapp.models import Document

filename = 'example.txt'
with open(filename, 'w') as file:
    file.write('This is an example file.\n')
    file.write('It was created using Python.\n')
    
doc = Document()
doc.file.save(filename, file)
doc.save()
```

We first create the file as before, then create a new `Document` instance and assign the file to the `file` field using its `save()` method. Finally, we save the `Document` instance to the database using its own `save()` method.

Note that we pass the filename and the file object separately to the `save()` method. The filename is used as the name of the file in the storage backend (such as the local filesystem or Amazon S3), while the file object is used to read the file contents and save them to the backend.

Handling file uploads from a form

To tie everything together and allow users to upload files through a form, we need to use Django's file handling capabilities in views and templates. Here is an example implementation:

```python
from django.shortcuts import render, redirect
from myapp.forms import DocumentForm

def upload_view(request):
    if request.method == 'POST':
        form = DocumentForm(request.POST, request.FILES)
        if form.is_valid():
            doc = form.save()
            return redirect('myapp:detail', pk=doc.pk)
    else:
        form = DocumentForm()
    return render(request, 'myapp/upload.html', {'form': form})
```

In this view, we check whether the request method is `POST` (which indicates that the form has been submitted). We then create a new `DocumentForm` instance and pass the request POST and FILES data to it. The `FILES` dictionary contains the uploaded files as `InMemoryUploadedFile` or `TemporaryUploadedFile` objects.

If the form is valid (which means that the file field is not empty and passes any validators specified in the form), we call the `save()` method on the form to create a new `Document` instance and save it to the database. We then redirect to another view to display the details of the newly created `Document`.

In the template for the form, we specify the form enctype as `multipart/form-data` to allow file uploads:

```html
<form method="post" enctype="multipart/form-data">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Upload</button>
</form>
```

The `form.as_p` template tag renders the form fields as paragraphs, and includes the file field as a file input element.

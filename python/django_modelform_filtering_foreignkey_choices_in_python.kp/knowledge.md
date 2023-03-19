---
title: What is the method to limit the available foreignkey choices in a django modelform?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the queryset attribute on the ForeignKey field in the ModelForm to filter the choices based on specific conditions.
---

**Contents**

[TOC]

Section 1: Introduction
When building a Django model form, there may be instances where you need to filter the possible ForeignKey choices presented to the user. This can be useful in limiting user input and reducing potential human error. In this tutorial, we will go through the steps to filter ForeignKey choices in a Django model form.

Section 2: Creating a ModelForm
The first step to filtering ForeignKey choices is to create a Django model form. Here is an example of a model form that includes a ForeignKey field:

```
from django import forms
from .models import Author, Book

class BookForm(forms.ModelForm):
    class Meta:
        model = Book
        fields = ('title', 'author',)
```

In this example, the `Book` model includes a ForeignKey field for the `Author` model. The `BookForm` inherits from `ModelForm` and specifies the `Book` model and the fields that are included in the form.

Section 3: Filtering ForeignKey Choices
To filter the possible ForeignKey choices for the `author` field, we need to override the field in the form's `__init__` method. Here is an example:

```
class BookForm(forms.ModelForm):
    def __init__(self, *args, **kwargs):
        user = kwargs.pop('user', None)
        super(BookForm, self).__init__(*args, **kwargs)
        if user:
            self.fields['author'].queryset = Author.objects.filter(user=user)
    
    class Meta:
        model = Book
        fields = ('title', 'author',)
```

In this example, we override the `author` field in the form's `__init__` method. We first retrieve the `user` argument passed to the form, and use it to filter the possible `Author` choices using the `filter` method. Finally, we set the filtered queryset back to the `author` field.

Section 4: Using the ModelForm
To use the filtered `BookForm`, we need to pass the current user to the form. Here is an example:

```
def create_book(request):
    if request.method == 'POST':
        form = BookForm(request.POST, user=request.user)
        if form.is_valid():
            book = form.save(commit=False)
            book.user = request.user
            book.save()
            return redirect('book-list')
    else:
        form = BookForm(user=request.user)

    return render(request, 'create_book.html', {'form': form})
```

In this example, we pass the current user to the `BookForm` when instantiating it. We can access the `user` argument in the form's `__init__` method to filter the possible `Author` choices.

With these steps, we have successfully filtered the ForeignKey choices in a Django ModelForm.

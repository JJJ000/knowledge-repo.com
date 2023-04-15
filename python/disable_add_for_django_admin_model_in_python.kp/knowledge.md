---
title: How to turn off the option to 'add' a specific model in django admin?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Override the ModelAdmin`s has\_add\_permission method and return False for a specific model.
---

**Contents**

[TOC]

Section 1 - Introduction:

Django provides a powerful administration interface to manage your application's data-level functionality. It includes various features, like adding, editing, and deleting data from models within the admin interface using a few simple clicks. However, sometimes you may want to restrict some users from adding data to a specific model. In this tutorial, we will discuss how to disable the 'Add' action for a specific model in Django's admin interface.

Section 2 - Steps to disable the 'Add' action for a specific model:

To disable the 'Add' action for a specific model, follow the below steps:

1. Subclass the `ModelAdmin` class for the model whose add action needs to be disabled.
2. Define the `has_add_permission()` method that will always return `False`.

Let's consider an example where we want to disable the 'Add' action for a model named `MyModel`. Below is the code snippet to achieve that:

```python
from django.contrib import admin
from .models import MyModel

class MyModelAdmin(admin.ModelAdmin):
    def has_add_permission(self, request):
        return False

admin.site.register(MyModel, MyModelAdmin)
```

In the above code, we are overriding the `has_add_permission()` method of `ModelAdmin` for the `MyModel`. This method decides whether to allow the user to add a new object or not. By returning `False`, we are disabling the 'Add' action for the `MyModel` in Django admin.

Section 3 - Verify the changes:

After making these changes, let's verify if the 'Add' button is disabled for `MyModel` in Django admin. To check it:

1. Log in as a superuser to the Django admin.
2. Navigate to the `MyModel` section.
3. Verify that the 'Add' button is disabled.

If you see that the 'Add' button is disabled, it means that you have successfully disabled the 'Add' action for a specific model.

Section 4 - Conclusion:

In this tutorial, we have discussed how to disable the 'Add' action for a specific model in Django's admin interface. In summary, we subclassed the `ModelAdmin` class for that specific model and overwritten the `has_add_permission()` method of that class to always return `False`. That's it, and by following these simple steps, we've disabled the 'Add' action for a particular Django model.

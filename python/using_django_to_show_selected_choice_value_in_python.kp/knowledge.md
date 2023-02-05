---
title: Show the selected option in django
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The value of a Choice field in Django can be accessed using the `value` attribute.
---

**Contents**

[TOC]

### Using the get_FOO_display() Method

In Django, the `get_FOO_display()` method is used to display the human-readable value of a field. This method is used on a model instance to return the value of a field that has choices set.

For example, if you have a model with a field `status` that has choices set:

```python
STATUS_CHOICES = [
    (1, 'active'),
    (2, 'inactive'),
]

class MyModel(models.Model):
    status = models.IntegerField(choices=STATUS_CHOICES)
```

You can display the human-readable value of the status field by calling the `get_status_display()` method on an instance of `MyModel`:

```python
instance = MyModel.objects.get(pk=1)
print(instance.get_status_display())  # 'active'
```

### Using the Choices Attribute

You can also access the choices attribute of a field to get the human-readable value of a field. This is useful when you don't have an instance of the model to call the `get_FOO_display()` method on.

For example, using the same model as above:

```python
value = 1
print(MyModel._meta.get_field('status').choices[value - 1][1])  # 'active'
```

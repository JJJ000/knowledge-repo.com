---
title: Attempting to add a mandatory 'new_field' to userprofile without a default value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is not possible to add a non-nullable field to userprofile without a default value in Python.
---

**Contents**

[TOC]

I. Introduction
To add a non-nullable field 'new_field' to userprofile without a default value in Python, you need to make some modifications to your Django models. 

II. Modify your models.py
Open your models.py file and make the following modifications:

```python
from django.db import models
from django.contrib.auth.models import User

class UserProfile(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    new_field = models.CharField(max_length=100, blank=False, null=False)
```

III. Create and Run Migrations
Now that you have modified your models.py file, it's time to create and run migrations to update your database schema. Follow these steps:
    
    1. Open your terminal or command prompt and navigate to your project directory.
    2. Enter the following command to create a new migration:
    
        `python manage.py makemigrations`
        
    3. Enter the following command to apply the migration:
    
        `python manage.py migrate`
        
IV. Update your Forms (Optional)
If you have created any forms that use the UserProfile model, you may need to update them to include the new_field. 

```python
from django import forms
from .models import UserProfile

class UserProfileForm(forms.ModelForm):
    class Meta:
        model = UserProfile
        fields = ('new_field',)
```

V. Conclusion
By following the steps outlined above, you should now have successfully added a non-nullable field 'new_field' to userprofile without a default in Python.

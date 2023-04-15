---
title: What is the process of transferring a model from one django app to another (django 1.7)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Copy the model file from one app to another and run `python manage.py makemigrations` and `python manage.py migrate` in the destination app.
---

**Contents**

[TOC]

## Section 1: Create a new app

The first step to moving a model between two Django apps is to create a new app in the destination app. This can be done using the following command:

```
python manage.py startapp new_app_name
```

This will create a new app in your Django project with the given name.


## Section 2: Copy the model

The next step is to copy the model from the source app to the new app. To do this, you can simply copy the model class from the source app's `models.py` file to the new app's `models.py` file. Make sure to also copy any related import statements.


## Section 3: Update the model's app label

Once the model has been copied over to the new app, you need to update the model's `app_label` attribute to match the name of the new app. This can be done by adding the following line of code to the model's definition:

```python
class ExampleModel(models.Model):
    # Define fields here

    class Meta:
        app_label = 'new_app_name'
```

Make sure to also import the new app's models module at the top of the file:

```python
from new_app_name.models import *
```


## Section 4: Run database migrations

Finally, you need to run database migrations to apply the changes you've made to the schema. Run the following command to create the migrations for the new app:

```
python manage.py makemigrations new_app_name
```

Then, run the following command to apply the migrations to the database:

```
python manage.py migrate new_app_name
```

After running these commands, the model should be moved to the new app and ready to use.

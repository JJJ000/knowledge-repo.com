---
title: How can a model field be renamed using south in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `migrate` command in South along with the `rename\_column` operation to rename a model field in Django.
---

**Contents**

[TOC]

## Introduction
South is a third-party migration tool for Django that allows you to manage database schema changes over time. It can help you to handle renaming or modifying fields in your models. In this tutorial, we will show you how to rename a model field using South in Django.

## Prerequisites
Before starting this tutorial, you should have a basic knowledge of Django and using models. You also need to make sure that you have installed and configured South in your project.

## Steps to Rename a Model Field using South
Here are the steps that you need to follow to rename a model field using South in Django:

### Step 1: Create a South Migration
First, you need to create a South migration by running the following command in your Django project's directory:

```
$ python manage.py schemamigration <your_app_name> --auto
```

This will create a new South migration file with the changes that you made to your models.

### Step 2: Edit the Migration File
Next, open up the migration file that was just created (located in your app's migration directory) and locate the `forwards` function. In this function, you need to add a new line to rename the model field. Here is an example of how to rename a field from `old_field_name` to `new_field_name`:

```python
db.rename_column('your_app_name_your_model_name', 'old_field_name', 'new_field_name')
```

### Step 3: Apply the Migration
After editing the migration file, you need to apply the migration by running the following command:

```
$ python manage.py migrate <your_app_name>
```

This will execute the migration and apply the changes to your database schema.

### Step 4: Check the Migration
Finally, you can check if the migration was successful by running the following command:

```
$ python manage.py sqlall <your_app_name>
```

This will show you the SQL statements that are executed to create the database schema. You should see that the old field name has been replaced with the new field name.


## Conclusion
In this tutorial, we showed you how to rename a model field using South in Django. By following the steps outlined above, you can manage database schema changes over time using South. If you encounter any errors or issues while renaming a model field, feel free to consult the South documentation or reach out to the Django community for help.

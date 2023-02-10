---
title: Using django 1.7+ to load initial data with data migrations
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Using Django`s built-in data migration framework, you can easily load initial data from a JSON file.
---

**Contents**

[TOC]

## Section 1: Creating a Data Migration 

Django 1.7+ comes with a built-in data migration system. This allows us to easily create migrations that can be used to load initial data into a database. To create a data migration, we must first create a migration file. This file is a Python class that inherits from the `django.db.migrations.Migration` class.

## Section 2: Adding Data to the Migration File 

Once we have created the migration file, we can add the data we want to load into the database. We can do this by using the `RunPython` method. This method takes two arguments: a function that will be executed when the migration is run, and a `reverse_code` function that will be used to undo the migration.

We can use the `RunPython` method to add our data to the database. We can use the `json.loads` function to parse our JSON data and then use the Django ORM to create database objects from the parsed data. 

## Section 3: Running the Migration 

Once we have added the data to the migration file, we can run the migration. To do this, we must use the `manage.py` command-line utility. This utility will detect the migration file, and execute it. This will add the data to the database. 

## Section 4: Testing the Migration 

Once the migration has been run, we should test it to make sure that the data was added correctly. We can do this by using the Django shell and querying the database. This will allow us to verify that the data was added correctly.

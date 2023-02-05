---
title: Comparing django model() and model.objects.create()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Model() creates an instance of a Model, while Model.objects.create() creates an instance of a Model and saves it to the database.
---

**Contents**

[TOC]

#### Django Model()

Django Model() is a class that is used to create a model. It is used to define the structure of the data that will be stored in the database. It is used to define the fields, their types, and any other information necessary to create the model.

#### Model.objects.create()

Model.objects.create() is a method used to create an object from the model. It is used to create an instance of the model and save it to the database. It takes the field values as arguments and creates an object with those values. It returns the created object.

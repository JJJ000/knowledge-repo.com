---
title: Is it possible to show the attributes of foreignkey fields in a django modeladmin's list_display?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, list\_display in a Django ModelAdmin can display attributes of ForeignKey fields.
---

**Contents**

[TOC]

**Yes**

**Using Related Field Lookups**

Django ModelAdmin’s list_display can be used to display attributes of ForeignKey fields in Python. This is done by using related field lookups. A related field lookup is a string that is used to specify the relationship between two models. For example, if a model has a ForeignKey to another model, the related field lookup would be the name of the foreign key field.

**Using the __str__ Method**

Another way to display attributes of ForeignKey fields in Python is to use the __str__ method. The __str__ method is a special method that is used to return a string representation of an object. This can be used to return the name of the ForeignKey field, or any other attribute that is associated with it.

**Using the ModelAdmin.list_display Attribute**

The ModelAdmin.list_display attribute can also be used to display attributes of ForeignKey fields. This attribute is a list of strings that specify which attributes of the model should be displayed in the admin interface. The strings can be the names of the fields, or the names of the related fields.

**Using the ModelAdmin.list_filter Attribute**

The ModelAdmin.list_filter attribute can also be used to display attributes of ForeignKey fields. This attribute is a list of strings that specify which attributes of the model should be used to filter the list of objects in the admin interface. The strings can be the names of the fields, or the names of the related fields.

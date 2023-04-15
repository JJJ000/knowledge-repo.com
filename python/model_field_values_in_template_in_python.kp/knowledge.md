---
title: Rephrase 
in the template, go through the field names and corresponding values of a model instance using iteration
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `instance.\_\_dict\_\_` attribute to access the dictionary of fields and values for the model instance in the template.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, Django is a popular web framework for building web applications. One of Django's features is the Model-View-Controller (MVC) architecture, which allows developers to create models that define the data structure of an application. Templates in Django are used to display this data to the user. In this article, we will discuss how to iterate over a model instance's field names and their corresponding values in a template.

Section 2: Getting Field Names and Values using the "instance" attribute
In Django, a model instance holds the values of fields defined in the model. We can access these values using the "instance" attribute. To get a list of field names of a model, we use the method "get_fields()" which returns a list of ModelField objects. Then, we can iterate over the list of fields and access their values using the instance attribute of the model. Here is an example of how to do this:

{% for field in instance._meta.get_fields %}
    <tr>
        <td>{{ field.verbose_name }}</td>
        <td>{{ field.value_from_object(instance) }}</td>
    </tr>
{% endfor %}

This code will iterate over all the fields of the model and display their verbose name and value in a table row.

Section 3: Using the built-in Django filter 
Another way to get the field names and values of a model instance is by using the built-in Django filter "items" that returns a list of (key, value) pairs that we can then iterate over. Here is an example of how to do this:

{% for key, value in instance.__dict__.items %}
    <tr>
        <td>{{ key }}</td>
        <td>{{ value }}</td>
    </tr>
{% endfor %}

This code will iterate over the instance dictionary that contains all the field names and values of the model instance and display them in a table row.

Section 4: Conclusion
Iterating over model instance field names and values in a template is a common operation in Django web applications. In this article, we discussed how to do this using the "instance" attribute and the built-in Django filter "items." With this knowledge, you can now display model instance data in a more customized way to your users.

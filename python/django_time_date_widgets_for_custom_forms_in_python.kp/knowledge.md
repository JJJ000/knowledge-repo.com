---
title: The utilization of django date/time widgets in personalized forms
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use Django`s built-in time/date widgets by importing them into your custom form class and setting them as the widget for the corresponding form field.
---

**Contents**

[TOC]

Section 1: Introduction to Django time/date widgets in custom form

Django time/date widgets are user interface components that help users input and manipulate date and time values in a form. These widgets come pre-built with Django and can be used in both built-in and custom forms. This article is focused on how to use Django time/date widgets in a custom form in Python. 

Section 2: How to use Django time/date widgets in a custom form in Python

Step 1: Importing dependencies
Before we can use Django time/date widgets in a custom form, we need to import the required dependencies. The following are the dependencies required to use Django time/date widgets in a custom form:

```python
from django import forms
from django.contrib.admin import widgets       
```

Step 2: Creating a custom form class
Next, we'll create a custom form class that inherits from Django's `forms.Form` class. In this step, we'll define the fields in our form and specify the widget to be used for each field.

```python
class CustomForm(forms.Form):
    date_field = forms.DateField(widget=widgets.AdminDateWidget)
    time_field = forms.TimeField(widget=widgets.AdminTimeWidget)
```
In the code snippet above, we defined two fields in our form (date_field and time_field) and specified the widgets to be used for each field. We used the `AdminDateWidget` and `AdminTimeWidget` widgets for the `date_field` and `time_field` fields, respectively.

Step 3: Rendering the form and widgets in a template
Now that we've defined our custom form and widgets, we need to render the form in a template. We'll use Django's built-in `render()` function to render the form and widgets in our template.

```python
from django.shortcuts import render

def custom_form(request):
    form = CustomForm()
    return render(request, 'custom_form.html', {'form': form})
```

In the code snippet above, we created a view function `custom_form()` that creates an instance of the `CustomForm` class and passes it to the `custom_form.html` template.

Step 4: Displaying the form and widgets in the template
Finally, we'll display the form and widgets in the template using Django's template language.

```html
{% extends "base.html" %}

{% block content %}
  <form method="post">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Submit</button>
  </form>
{% endblock %}
```
In the code snippet above, we used the `{{ form.as_p }}` template tag to render the form as a series of paragraphs, with each form field rendered using its associated widget.

Section 3: Conclusion

In this article, we've shown how to use Django time/date widgets in a custom form in Python. By using Django time/date widgets, you can improve the user experience of your forms and make it easier for users to input and manipulate date and time values. If you're interested in learning more about Django forms, check out the official Django documentation.

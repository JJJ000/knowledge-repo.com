---
title: What is the process of adding a placeholder in django's charfield?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can add a placeholder on a CharField in Django by using the `widget` attribute and setting its `attrs` dictionary with a `placeholder` key and a string value.
---

**Contents**

[TOC]

## 1. Overview
A placeholder is a text that appears in a form field until the user starts typing. It can give the user context and guidance on what information is expected to be entered in the field. In Django, placeholders can be added to CharField using widgets.

## 2. Creating a Widget
To add a placeholder to a CharField, we need to create a widget that inherits from Django's `TextInput` widget. The widget should have a `placeholder` attribute that can be set to the desired placeholder text.

```python
from django.forms.widgets import TextInput

class PlaceholderInput(TextInput):
    def __init__(self, attrs=None, placeholder=None):
        super().__init__(attrs)
        self.attrs.update({'placeholder': placeholder})
```

## 3. Using the Widget
Once we have our widget, we can use it in a form by specifying it as the widget for the desired field. In the `Meta` class of the form, we can override the field definition and set the widget to our custom `PlaceholderInput`.

```python
from django import forms

class MyForm(forms.Form):
    my_field = forms.CharField(
        max_length=100,
        widget=PlaceholderInput(attrs={'class': 'my-class'}, placeholder='Type your text here')
    )
```

## 4. Displaying the Form
Finally, we need to render the form in a template. The `{{ form }}` template tag will render the form with all its fields and labels.

```html
<form method="post">
  {% csrf_token %}
  {{ form.as_p }}
  <button type="submit">Submit</button>
</form>
```

When the form is rendered, the `my_field` input will have a placeholder text that says "Type your text here".

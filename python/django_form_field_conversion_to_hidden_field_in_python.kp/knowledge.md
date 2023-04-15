---
title: Convert a form field in django into a hidden field
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Set the widget attribute of the form field to forms.HiddenInput().
---

**Contents**

[TOC]

## Retrieving the Form Field

Before we can change a Django form field to a hidden field, we first need to retrieve the form field we want to modify. This can be done in several ways, depending on your specific use case. Some common options include:

- Accessing the field through the form's `fields` dictionary
- Accessing the field through the form's `declared_fields` attribute
- Creating a new form subclass that overrides the field in question

Once you have a reference to the form field you want to modify, you can proceed with making the necessary changes.

## Changing the Field Widget

To change a Django form field to a hidden field, we need to change the field's widget. Widgets are responsible for rendering HTML input elements for a given form field. Changing the widget for a field can be done by setting the field's `widget` attribute to an instance of the new widget you want to use. For example, to change a text input field to a hidden input field, you could do:

```
from django import forms

class MyForm(forms.Form):
    my_field = forms.CharField()

# Retrieve the form field we want to modify
my_field = MyForm.declared_fields['my_field']

# Set the field's widget to a hidden input widget
my_field.widget = forms.HiddenInput()
```

This will change the `my_field` text input field to a hidden input field.

## Modifying Widget Attributes

In some cases, you may need to modify widget attributes when changing a Django form field to a hidden field. For example, you might need to set the `value` attribute of the hidden input field to a specific value. This can be done by setting the widget attribute's specific attribute. For example:

```
# Modify the hidden input widget to set the value attribute
my_field.widget.attrs['value'] = 'my-default-value'
```

This will set the `value` attribute of the hidden input field to `'my-default-value'`.

## Conclusion

Changing a Django form field to a hidden field requires retrieving the field, changing its widget to a hidden input widget, and potentially modifying widget attributes as needed. By following these steps, you can easily modify your Django forms to include hidden fields as needed.

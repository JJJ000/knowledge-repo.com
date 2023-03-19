---
title: What is the way to traverse a dictionary inside another dictionary in a django template?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use nested dictionary keys and dot notation to access the values in the template, for example, {{ outer\_dict.inner\_dict.key }}.
---

**Contents**

[TOC]

## Section 1: Introduction
Iterating through a dictionary in a dictionary in Django template involves accessing nested dictionary values and keys. This can be done by nesting loops and referencing the appropriate keys in the dictionary. 

## Section 2: Accessing nested dictionary values in Django template
To access nested dictionary values, we need to first access the parent dictionary and then the child dictionary. We can do this by using the dot operator in Django template. For example, if we have a dictionary structure like this:

```python
my_dict = {
    'first_dict': {
        'name': 'John',
        'age': 30
    },
    'second_dict': {
        'name': 'Jane',
        'age': 25
    }
}
```

We can access the name and age of the first_dict by using the following syntax:

```html
{{ my_dict.first_dict.name }}
{{ my_dict.first_dict.age }}
```

## Section 3: Nested loops in Django template
To iterate through a dictionary in a dictionary, we need to use nested loops in the Django template. We iterate over the parent dictionary first and then iterate over the child dictionary. For example, if we have a dictionary structure like this:

```python
my_dict = {
    'first_dict': {
        'name': 'John',
        'age': 30
    },
    'second_dict': {
        'name': 'Jane',
        'age': 25
    }
}
```

We can loop over the parent dictionary and then access the child dictionary using the following syntax:

```html
{% for key, value in my_dict.items %}
    {% for sub_key, sub_value in value.items %}
        {{ sub_key }}: {{ sub_value }}
    {% endfor %}
{% endfor %}
```

## Section 4: Conclusion
By using the above syntax, we can iterate through a dictionary in a dictionary in Django template. This can be useful when we have a hierarchical data structure that we want to display in a view.

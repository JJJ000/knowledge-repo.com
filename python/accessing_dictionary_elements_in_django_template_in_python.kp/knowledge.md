---
title: What is the process of accessing a dictionary element within a django template?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To access a dictionary element in a Django template, use the `dot` notation followed by the key name, like this {{ my\_dict.key\_name }}.
---

**Contents**

[TOC]

# Introduction

Django templates are used to render dynamically generated HTML pages. A typical template consists of static HTML with placeholders that are populated with dynamic content when the template is rendered. One common use case for templates is rendering dictionaries that have been passed from a Django view.

In this tutorial, we will look at how you can access a dictionary element in a Django template.


# Step 1: Passing a dictionary to a Django template

In order to access a dictionary element in a Django template, we must first pass the dictionary to the template from a Django view. Here's an example:

```python
def my_view(request):
    my_dict = {'key1': 'value1', 'key2': 'value2'}
    return render(request, 'my_template.html', {'my_dict': my_dict})
```

In this example, we have a view called `my_view` that creates a dictionary called `my_dict` with two key-value pairs. We then pass `my_dict` to a template called `my_template.html` using the `render()` method.


# Step 2: Accessing a dictionary element in a Django template

Once we have passed a dictionary to a Django template, we can access its elements using dot notation. Here's an example:

```html
<p>Key 1: {{ my_dict.key1 }}</p>
<p>Key 2: {{ my_dict.key2 }}</p>
```

In this example, we have two paragraphs that access the `key1` and `key2` elements of `my_dict`, respectively. The dot notation is used to access dictionary elements in the Django template language.


# Step 3: Using dictionary elements in template logic

In addition to accessing dictionary elements directly in a Django template, we can also use them in template logic. Here's an example:

```html
{% if my_dict.key1 %}
  <p>Key 1 exists and has value "{{ my_dict.key1 }}".</p>
{% else %}
  <p>Key 1 does not exist.</p>
{% endif %}
```

In this example, we use the `{% if %}` template tag to check if the `key1` element exists in `my_dict`. If it does, we output a paragraph that states the key exists and displays its value. Otherwise, we output a different paragraph that indicates the key does not exist.


# Conclusion

Accessing dictionary elements in a Django template is straightforward using dot notation. By passing a dictionary to a template from a view, we can access its elements directly in the template or use them in template logic. By following these steps, you can easily access dictionary elements in your Django templates.

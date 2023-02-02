---
title: Find the length of each item in a list using a jinja2 template
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: In a Jinja2 template, the lengths of a list can be retrieved using the `length` filter.
---

**Contents**

[TOC]

## Section 1: Creating the List

In order to get the lengths of a list in a Jinja2 template, we must first create the list. This can be done by declaring a variable and setting it equal to a list of items. For example:

```python
my_list = ["apple", "banana", "carrot"]
```

## Section 2: Rendering the Template

Next, we need to render the Jinja2 template. This can be done by creating a template object and passing in the list variable as a context. For example:

```python
from jinja2 import Template

template = Template("My list has {{ my_list|length }} items.")

rendered_template = template.render(my_list=my_list)

print(rendered_template)
```

This will print out `My list has 3 items.`

## Section 3: Accessing the List Length

Finally, we can access the list length in the template by using the `length` filter. This filter will return the number of items in the list. For example:

```jinja2
My list has {{ my_list|length }} items.
```

This will render as `My list has 3 items.`

## Section 4: Conclusion

In conclusion, getting the lengths of a list in a Jinja2 template is relatively simple. All we need to do is create the list, render the template with the list as a context, and then use the `length` filter to access the list length.

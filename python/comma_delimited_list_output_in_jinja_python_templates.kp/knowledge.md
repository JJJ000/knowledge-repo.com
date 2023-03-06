---
title: What is the way to generate a list separated by commas in jinja Python templates?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `join` filter with a comma separator on a list or tuple.
---

**Contents**

[TOC]

## Section 1: Introduction to Jinja and Python Template
Jinja is a template engine for Python programming language. It is used to separate the application logic from the presentation logic. Many web frameworks use Jinja2 to render templates. A template engine enables us to render dynamic content by providing dynamic data to the template. In this tutorial, we will learn how to output a comma delimited list in Jinja2 Python template.


## Section 2: Creating a Jinja2 Python Template
To create a Jinja2 Python template, we need to install the Jinja2 module. Run the following command to install the Jinja2 module:

```
pip install Jinja2
```

After installing the Jinja2 module, create a template file with extension .html. Let’s create a template file named list.html.

```
<!DOCTYPE html>
<html>
    <head>
        <title>List Template</title>
    </head>
    <body>
        <h1>List of Items</h1>
        <ul>
            {% for item in items %}
                <li>{{ item }}</li>
            {% endfor %}
        </ul>
    </body>
</html>
```

In the above code, we have a variable named items which is passed to the template to render a list of items. The items are displayed in an unordered list (ul) with li tags.


## Section 3: Creating a Python Script to Render the Template
In this step, we create a Python script to render the template. First, we import the Jinja2 module and load the template file using the environment class.

```
from jinja2 import Environment, FileSystemLoader

file_loader = FileSystemLoader('templates')
env = Environment(loader=file_loader)
template = env.get_template('list.html')
```

In the above code, we are creating a FileSystemLoader object with the ‘templates’ directory as the loader. We then create an Environment object with the file_loader object as the loader. Next, we load the list.html template file using the get_template() method and save it in the template variable


## Section 4: Rendering the Template with Dynamic Data
In the final step, we render the template with dynamic data. We create a Python list containing the items, and we pass this list to the template.

```
items = ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5']
output = template.render(items=items)
print(output)
```

In the above code, we create a list named items with 5 items. Next, we render the template by calling the render() method on the template variable and passing the items variable as a parameter with the name ‘items’. Finally, we print the rendered output. The output will contain a list of items separated by a comma.

---
title: Could you suggest a simpler method for embedding html in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The easiest way to escape HTML in Python is to use the html.escape() function.
---

**Contents**

[TOC]

Section 1: Introduction

HTML injection attacks are among the most common web security vulnerabilities. To prevent these attacks, it is necessary to escape HTML characters in your Python code. In this article, we will explore the easiest ways to escape HTML in Python.

Section 2: Using the html module

The html module in Python provides a set of functions to convert text to HTML-safe code. The escape() function is the most commonly used function in this module. It converts special characters like '<' and '>' to their corresponding HTML entities, preventing them from being treated as HTML tags.

```python
import html

text = "<h1>Hello, World!</h1>"
escaped_text = html.escape(text)

print(escaped_text)
```

Output:
```html
&lt;h1&gt;Hello, World!&lt;/h1&gt;
```

Section 3: Using the cgi module

The cgi module in Python provides another method to escape HTML. The escape() function in this module works similar to the escape() function in the html module.

```python
import cgi

text = "<h1>Hello, World!</h1>"
escaped_text = cgi.escape(text)

print(escaped_text)
```

Output:
```html
&lt;h1&gt;Hello, World!&lt;/h1&gt;
```

Section 4: Using Jinja2 templates

If you're using a template engine like Jinja2 in your Python code, you can escape HTML using the autoescape extension. This extension automatically escapes all variables in the template, preventing HTML injection attacks.

```python
from jinja2 import Environment, PackageLoader, select_autoescape

env = Environment(
    loader=PackageLoader('myapp', 'templates'),
    autoescape=select_autoescape(['html', 'xml'])
)

template = env.get_template('mytemplate.html')

data = {
    'title': '<h1>Hello, World!</h1>'
}

output = template.render(**data)

print(output)
```

Output:
```html
<!DOCTYPE html>
<html>
<head>
	<title>&lt;h1&gt;Hello, World!&lt;/h1&gt;</title>
</head>
<body>
	<h1>Hello, World!</h1>
</body>
</html>
```

In this example, the autoescape extension is set to escape both HTML and XML characters. This ensures that all variables in the template are automatically escaped, preventing any HTML injection attacks.

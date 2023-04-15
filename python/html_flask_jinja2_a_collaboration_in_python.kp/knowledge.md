---
title: Transferring html to the template through flask/jinja2
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can pass HTML to a template using Flask/Jinja2 in Python by using the |safe filter in the template.
---

**Contents**

[TOC]

Section 1: Introduction to Flask

Flask is a Python-based micro web framework that allows flexible and scalable web application development. Flask provides integration with Jinja2 templating engine, which facilitates easy-to-use HTML generation.

Section 2: Passing HTML to a Template

In order to pass HTML to a Flask template using Jinja2, you can use the render_template function from the Flask module.

First, import the Flask module and create a Flask object:

```python
from flask import Flask, render_template

app = Flask(__name__)
```

Next, create a route function that will render a template containing the HTML code:

```python
@app.route('/')
def index():
    html_code = "<h1>Hello, World!</h1>"
    return render_template('index.html', html_code=html_code)
```

In this example, the index function is called when the root endpoint is accessed. The `html_code` variable contains the HTML code that will be passed to the template. The `render_template` function renders the `index.html` template and passes the `html_code` variable to it.

Section 3: Using Jinja2 to Include HTML Code in a Template

Jinja2 is a powerful templating engine that allows you to include HTML code in a template. You can use the `{{ variable }}` notation to render the value of a variable in the template.

In our example, we will include the `html_code` variable in the template using Jinja2:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Flask Template Example</title>
</head>
<body>
    <div>
        {% raw %}
        {{ html_code }}
        {% endraw %}
    </div>
</body>
</html>
```

The `{% raw %}` and `{% endraw %}` tags are used to tell Jinja2 to treat the HTML code between them as raw text, disabling any Jinja2 processing.

Section 4: Conclusion

In this tutorial, we have seen how to pass HTML code to a Flask template using Jinja2. By leveraging the power of Flask and Jinja2, you can easily create rich and dynamic web applications.

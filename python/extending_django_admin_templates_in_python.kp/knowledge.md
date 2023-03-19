---
title: What are the steps to modify and enhance the fundamental django admin templates?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To override and extend basic Django admin templates in Python, create a new template file in your project`s templates/admin directory with the same name as the template file you want to override, modify it as needed, and load it using the {% extends %} and {% include %} template tags as necessary.
---

**Contents**

[TOC]

# Introduction

Django's admin interface comes with a set of pre-built templates that provide a basic design and layout to all admin pages. However, sometimes you may need to customize these templates to match your project requirements. In this tutorial, we will explore the process of overriding and extending the basic Django admin templates using Python.

## Finding the Base Templates

Before we start overriding the Django admin templates, we need to locate where the base templates are located. Django provides a built-in `app_directories` backend to search for templates in all installed apps. To locate the admin templates, we can add the following code to our project's settings.py file:

```
# settings.py

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            # ...
        },
    },
]

# To find the location of the Django admin templates
import os
from django.conf import settings
print(os.path.join(settings.BASE_DIR, 'templates/admin'))
```

Running this code should output the absolute path to the admin templates directory.

## Overriding Admin Templates

To override a specific admin template, we can create a new template with the same name and directory structure in our app's templates directory. For example, to override the admin site header template, we can create a new template `templates/admin/base_site.html`.

```
<!-- base_site.html -->

{% extends "admin/base.html" %}

{% block title %}
    {{ title }} | {{ site_title|default:_('Django site admin') }}
{% endblock %}

{% block branding %}
    <h1 id="site-name"><a href="{% url 'admin:index' %}">{{ site_header|default:_('Django administration') }}</a></h1>
{% endblock %}
```

Now, Django will use this new template instead of the default one. We can similarly override other templates such as login, change list, edit forms, etc. by creating new templates in our app's templates/admin directory with the same names as the default templates.

## Extending Admin Templates

Sometimes, we may want to add or modify some content in the existing admin templates, without completely overriding them. In such cases, we can use template inheritance to extend the base templates and add our own content.

For example, let's say we want to add a custom link to the top menu in the admin site header. We can create a new template `templates/admin/custom_header.html` and extend the `base_site.html` template.

```
<!-- custom_header.html -->

{% extends "admin/base_site.html" %}

{% block extrahead %}
    {{ block.super }}
    <link rel="stylesheet" type="text/css" href="{% static 'css/custom.css' %}">
{% endblock %}

{% block branding %}
    {{ block.super }}
    <a href="#">Custom Link</a>
{% endblock %}
```

In this example, we have added a new `extrahead` block to add some custom CSS and extended the `branding` block to add our custom link to the site header.

## Conclusion

In this tutorial, we learned how to override and extend the basic Django admin templates using Python. By customizing these templates, we can create a unique admin interface that matches our project requirements. If you want to learn more about Django's template system, check out the official documentation.

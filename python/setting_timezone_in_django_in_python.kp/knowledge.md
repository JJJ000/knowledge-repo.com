---
title: What is the process for configuring the timezone in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Set the timezone in Django by changing the value of the TIME\_ZONE key in the settings.py file.
---

**Contents**

[TOC]

## Introduction

Django is a popular web framework written in Python. When developing web applications, it is important to correctly set the timezone for your project. This ensures that any date and time values displayed to users are accurate and consistent.

In this article, we will discuss the steps necessary to set the timezone in Django.

## Step 1: Install pytz

Before setting the timezone in Django, you need to install the `pytz` library, which provides the necessary tools to work with time zones.

You can install `pytz` using pip:

```
pip install pytz
```

## Step 2: Edit the settings.py file

To set the timezone in Django, you need to edit the `settings.py` file in your Django project.

In the file, locate the `TIME_ZONE` setting and change its value to the timezone you want to use. For example, if you want to use the US Eastern Timezone, you can set the value to:

```
TIME_ZONE = 'America/New_York'
```

You can find a list of supported timezone values in the Pytz documentation.

## Step 3: Restart the Django development server

After editing the `settings.py` file, you need to restart the Django development server to apply the changes.

To do this, stop the server by pressing `Ctrl+C` in the terminal window, and then start it again using the `python manage.py runserver` command.

## Step 4: Verify the timezone

To verify that the timezone has been set correctly, you can create a simple Django view that displays the current time.

First, import the `datetime` and `pytz` libraries:

```python
from datetime import datetime
import pytz
```

Then, in your view, create a `datetime` object and apply the timezone using `pytz`:

```python
now = datetime.now(pytz.timezone('America/New_York'))
```

Finally, display the time in your HTML template:

```html
<p>The current time is {{ now }}</p>
```

When you load your view in a web browser, you should see the current time displayed in the specified timezone.

## Conclusion

Setting the timezone in Django is a simple process that can greatly improve the accuracy and consistency of date and time values in your web application. By following the steps outlined in this article, you can ensure that your Django project is displaying time correctly.

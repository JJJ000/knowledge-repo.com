---
title: What is the syntax for viewing the unprocessed sql queries that django is executing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the Django Debug Toolbar to view the raw SQL queries Django is running.
---

**Contents**

[TOC]

### Using Python's logging Module

The simplest way to view the raw SQL queries that Django is running is to use Python's logging module. You can configure Django to log all queries to the console by adding the following lines to your settings.py file:

```
LOGGING = {
    'version': 1,
    'disable_existing_loggers': False,
    'handlers': {
        'console': {
            'level': 'DEBUG',
            'class': 'logging.StreamHandler',
        },
    },
    'loggers': {
        'django.db.backends': {
            'handlers': ['console'],
            'level': 'DEBUG',
        },
    }
}
```

Once this is done, all queries will be logged to the console.

### Using Django Debug Toolbar

Another way to view the raw SQL queries that Django is running is to use the Django Debug Toolbar. This is a third-party package that provides a web-based interface for viewing Django queries.

To install the Django Debug Toolbar, you first need to install the package via pip:

```
pip install django-debug-toolbar
```

Once the package is installed, you can add the toolbar to your project by adding the following lines to your settings.py file:

```
INSTALLED_APPS = [
    ...
    'debug_toolbar',
]
```

You can then enable the toolbar by adding the following lines to your urls.py file:

```
if settings.DEBUG:
    import debug_toolbar
    urlpatterns = [
        ...
        path('__debug__/', include(debug_toolbar.urls)),
    ] + urlpatterns
```

Once the toolbar is enabled, you can view all queries that Django is running by navigating to the debug toolbar URL.

### Using Django Shell

Finally, you can view the raw SQL queries that Django is running by using the Django shell. This is a command-line interface for interacting with Django.

To use the Django shell, you first need to open a terminal window and navigate to your project directory. You can then start the Django shell by running the following command:

```
python manage.py shell
```

Once the shell is open, you can use the ```connection.queries``` attribute to view all queries that Django is running.

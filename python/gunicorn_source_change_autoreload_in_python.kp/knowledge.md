---
title: Auto-reload of gunicorn upon modification of source code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Gunicorn does not provide built-in autoreload functionality, but it can be achieved through third-party libraries such as watchdog or run\_with\_reloader.
---

**Contents**

[TOC]

Section 1: Introduction
Gunicorn is Python's WSGI HTTP Server which enables the user to run Python Web Applications. One of the main features of Gunicorn is autoreload which allows the server to reload the source code and restart itself when any changes made to the server code. 

Section 2: How autoreload works in Gunicorn?
The autoreload feature is present in Gunicorn from its version 19.3 onwards. Once you start the Gunicorn server, you can enable the autoreload feature by adding the "--reload" command-line option to the Gunicorn command. 

```
gunicorn --reload myapp:app
```

This command will start the Gunicorn server for the application "myapp" with the "app" Flask or WSGI callable object. Once the autoreload feature is enabled, the Gunicorn server will reload itself whenever any changes made to the application source code.

Section 3: Enabling autoreload for specific modules
The Gunicorn autoreload feature reloads the entire source code of the application whenever any changes made to the code. But sometimes, we may want to apply the reload only to specific modules of the application. 

To enable autoreload for specific modules, we can use the "--reload-extra-file" command-line option. 

```
gunicorn --reload myapp:app --reload-extra-file my_module.py
```

This command will start the Gunicorn server for the application "myapp" with the "app" Flask or WSGI callable object. In addition to that, only the changes made in "my_module.py" will be detected, and the server will reload itself whenever any changes made to the module.

Section 4: Conclusion
The autoreload feature in Gunicorn is an excellent tool for developers to increase their productivity by eliminating the need for manually restarting the server on every code change. We can enable the autoreload feature in Gunicorn by adding the "--reload" command-line option or "--reload-extra-file" option for specific module reloads.

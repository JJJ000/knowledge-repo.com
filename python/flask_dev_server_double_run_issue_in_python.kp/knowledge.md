---
title: What is the reason for flask dev server running itself twice?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The Flask dev server has an auto-reload feature that starts a new instance of the server to reflect changes made to the code.
---

**Contents**

[TOC]

Possible answer:

Introduction
------------

Flask is a popular Python web framework that allows developers to build web applications using a simple and flexible approach. One of the core components of Flask is the built-in development server, which is designed to make it easy to test and debug Flask applications during development. However, newcomers to Flask may be surprised to find that running the Flask dev server often results in the server starting up twice, as if the server is running itself twice. In this answer, we explore the reasons for this behavior and how to avoid it.

Flask application structure
---------------------------

Before we can understand why the Flask dev server runs itself twice, we need to understand the basic structure of a Flask application. In Flask, an application is defined by creating an instance of the Flask class, which provides a container for the application's routes, views, templates, and other components. Typically, a Flask application is defined in a Python module, which might be named `app` or `server` or something else. The module usually contains three main parts:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'Hello, world!'
```

First, we import the Flask class from the `flask` module. Then, we create an instance of the Flask class and assign it to a variable named `app`. The argument `__name__` tells Flask where to find the root directory of the application (usually the directory where the Python module is located). Finally, we define a simple route using the `@app.route()` decorator, which associates a URL path ("/") with a view function (in this case, `index()`).

Running the Flask dev server
----------------------------

To run a Flask application in development mode, we usually use the built-in `flask` command-line tool, which provides several useful commands for managing a Flask project. One of these commands is `run`, which starts the Flask dev server and listens for incoming requests. For example:

```
$ export FLASK_APP=app.py  # or whatever your Flask app is called
$ flask run
```

Under the hood, the `flask run` command does several things:

1. It imports the Flask application from the module specified in the `FLASK_APP` environment variable.
2. It sets the `FLASK_ENV` environment variable to "development" if it wasn't already set.
3. It starts a WSGI server (such as Werkzeug) to handle incoming requests.
4. It registers a signal handler to stop the server when you press Ctrl+C.

The crucial point here is that when Flask imports the application module (step 1), it executes all the code in the module, including the creation of the Flask app instance and the registration of routes, views, etc. This means that the Flask dev server effectively runs the entire Flask application as soon as it starts up.

Why the Flask dev server runs twice
-----------------------------------

So why does the Flask dev server run itself twice, instead of just once? The answer is that when you run the `flask run` command, Flask actually imports the application module twice, in two different modes:

1. Firstly, Flask imports the application module in "import" mode, which means that it executes all the code in the module, but doesn't start the server yet. This is necessary to ensure that all the views, routes, templates, and other components of the application are properly registered with Flask and available to the WSGI server.
2. Then Flask imports the application module again in "run" mode, which means that it runs the entire application code again, including starting the WSGI server and serving requests.

This two-step process might seem redundant, but it actually has some benefits:

- It ensures that the Flask application is fully initialized before the WSGI server starts, which can help prevent errors and race conditions.
- It allows the Flask dev server to automatically reload the application code when it changes, without having to restart the entire server.
- It makes it easier to debug the Flask application code, since you can use the Python debugger to step through the code that Flask runs in "import" mode.

How to avoid the double start
-----------------------------

If you find that the Flask dev server is running the application code twice, you might want to disable the automatic reloader, which is responsible for reloading the application code when it changes. To do this, you can pass the `--no-reload` option to the `flask run` command:

```
$ flask run --no-reload
```

Alternatively, you can set the `FLASK_RUN_RELOAD` environment variable to `0` before running the `flask run` command:

```
$ export FLASK_RUN_RELOAD=0
$ flask run
```

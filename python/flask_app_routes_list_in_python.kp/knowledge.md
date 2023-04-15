---
title: Obtain a comprehensive inventory of the routes specified in the flask application
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To get a list of all routes defined in the Flask app in Python, we can use the `url\_map` attribute of the Flask application object.
---

**Contents**

[TOC]

## Section 1: Introduction

In Flask, routes are defined using the `@app.route()` decorator, where `app` is an instance of the Flask class. Flask applications can have multiple routes defined for different URLs. In this tutorial, we will discuss several ways of getting a list of all routes defined in an app in Python.

## Section 2: Using Flask-built-in method

Flask provides a built-in method `app.url_map.iter_rules()` to get a list of all routes defined in an app. Here is an example:

```python
from flask import Flask

app = Flask(__name__)

# define some routes
@app.route('/')
def index():
    return 'Hello, World!'

@app.route('/about')
def about():
    return 'About us'

# get all routes
all_routes = app.url_map.iter_rules()

# print all routes
for route in all_routes:
    print(route)
```

Output:
```
/
/about
```

In the above example, we first define two simple routes `/` and `/about`. Then we use `app.url_map.iter_rules()` to get all the routes, and iterate over them to print out the route endpoint.

## Section 3: Using Flask-Script

Flask-Script is a Flask extension that provides support for writing external scripts in Flask. One of its commands, `urlmap`, can be used to print out a list of all routes defined in the app. Here is an example:

```python
from flask import Flask
from flask_script import Manager

app = Flask(__name__)
manager = Manager(app)

# define some routes
@app.route('/')
def index():
    return 'Hello, World!'

@app.route('/about')
def about():
    return 'About us'

if __name__ == '__main__':
    manager.run()
```

To run the `urlmap` command, we execute the script with an additional command `urlmap`. Here's how to do it:

```
$ python my_script.py urlmap
```

Output:
```
Endpoint                           Methods  Rule
---------------------------------  -------  -----------------------
about                              GET      /about
static                             GET      /static/<path:filename>
index                              GET      /
```

In the above example, we first define two simple routes `/` and `/about`. Then we use `Manager(app)` to create a manager instance for the app. The manager instance provides various commands such as `urlmap`. When the script is executed with `urlmap` command, it prints out all the routes and their respective endpoints.

## Section 4: Using Flask-Route-List

Flask-Route-List is a Flask extension that provides a command `flask routes` to list all the routes that has been defined. It can be easily installed using pip:

```
$ pip install flask-route-list
```

Here is an example of how to use it:

```python
from flask import Flask
from flask_route_list import show_routes

app = Flask(__name__)

# define some routes
@app.route('/')
def index():
    return 'Hello, World!'

@app.route('/about')
def about():
    return 'About us'

# print all routes
show_routes(app)
```

Output:
```
URL                       NAME    METHODS
-----------------------  ------  --------
/                         index   GET
/about                    about   GET
```

In the above example, we first define two simple routes `/` and `/about`. Then we use `show_routes()` function from `flask_route_list` to print out all the routes with their names and supported methods.

## Conclusion

In this tutorial, we have discussed three ways of getting a list of all routes defined in a Flask app. The first approach used the built-in `app.url_map.iter_rules()` method, the second approach used Flask-Script extension, and the third approach used Flask-Route-List extension. All these approaches are easy to use and provide all the necessary information about the defined routes.

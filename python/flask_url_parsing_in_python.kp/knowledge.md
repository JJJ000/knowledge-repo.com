---
title: What is the process of extracting the various components of a flask request's url?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the request module from Flask to access various parts of a request URL in Python, such as the path, query parameters, and fragment identifier.
---

**Contents**

[TOC]

# Introduction

When building a Flask application, it is common to need to extract information from a request's URL. Flask provides various methods to access different parts of a request’s URL. This article will discuss different methods to get the different parts of a Flask request’s URL in Python. 

# Method 1: Using request.path

The request.path attribute returns the URL path that triggered the request. For example, if the requested URL is www.example.com/products, the request.path would be /products. 

Here’s an example:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/products')
def products():
    path = request.path
    return f"The requested path is: {path}"

if __name__ == '__main__':
    app.run(debug=True)
```

Output: 

```
The requested path is: /products
```

# Method 2: Using request.full_path

The request.full_path attribute returns the full URL of the request, including the query parameters. 

Here’s an example:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/products')
def products():
    full_path = request.full_path
    return f"The requested URL is: {full_path}"

if __name__ == '__main__':
    app.run(debug=True)
```

Output: 

```
The requested URL is: /products?page=1&sort=price
```

# Method 3: Using request.args

The request.args property returns a `MultiDict` containing all the query parameters of the request URL. It can be used to extract any query parameter of the request.

Here’s an example:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/search')
def search():
    query = request.args.get('query')
    sort = request.args.get('sort')
    return f"Query: {query}, Sort: {sort}"

if __name__ == '__main__':
    app.run(debug=True)
```

Here's how you can test the above endpoint: 

```
http://127.0.0.1:5000/search?query=Python&sort=price
```

Output: 

```
Query: Python, Sort: price
```

# Conclusion

In this article, we discussed various methods to extract different parts of a Flask request’s URL. We used request.path to extract the URL path, request.full_path to extract the full URL, and request.args to extract the query parameters. By combining these methods, we can easily extract any part of a request’s URL in Python.

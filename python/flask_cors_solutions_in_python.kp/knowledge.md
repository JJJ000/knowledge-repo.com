---
title: Resolve the issue of cross origin resource sharing using flask
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Enable CORS by installing the flask-cors library and importing it to your Flask app.
---

**Contents**

[TOC]

## What is Cross-Origin Resource Sharing (CORS)?

Cross-Origin Resource Sharing (CORS) is a security feature that is used to restrict web pages or applications from accessing resources from another domain or location. This is implemented by browsers to prevent malicious attacks like cross-site scripting (XSS) and cross-site request forgery (CSRF).

## The Problem with Flask and CORS

Flask, being a web framework, allows you to create web applications, but by default, it doesn't handle CORS issues. This means that if you send a HTTP request to a Flask server from a different domain, the browser may block the request, as the server's response may contain headers that indicate the request should be blocked or restricted.

## Solutions for CORS with Flask

### Solution 1: Flask-CORS Extension

Flask-CORS is a Flask extension that handles Cross-Origin Resource Sharing (CORS) making cross-origin AJAX requests possible out-of-the-box. Flask-CORS supports all standard CORS headers and request methods and also provides a means to handle non-standard CORS headers.

To use Flask-CORS, you'll need to install it:

```python
pip install flask-cors
```

Once installed, you can use it in your Flask application like this:

```python
from flask_cors import CORS

app = Flask(__name__)
CORS(app)
```

Using this method, Flask-CORS will handle all CORS-related issues and you can make cross-domain requests easily.

### Solution 2: Use Response Headers

Another way to handle CORS issues with Flask is to manually override the CORS-related headers in the response object. This can be done through the use of response headers.

For example, to allow all domains to access your Flask server, you can add the following headers in your response:

```python
@app.route('/')
def index():
    response = make_response('Hello, World!')
    response.headers['Access-Control-Allow-Origin'] = '*'
    return response
```

This will allow any domain to access your Flask server and make cross-domain requests.

### Solution 3: Use Proxy Server

Another solution for CORS issues is to use a proxy server to handle the requests. A proxy server acts as an intermediary between the client and the server, and makes requests on behalf of the client.

To use a proxy server for handling CORS issues, you can create a separate Flask application that will act as the proxy server. This application will receive requests from the client and make requests to the original server on behalf of the client. The response from the original server will then be passed back to the client.

This approach is more involved as it requires creating a separate Flask application for the proxy server, but it provides more control over how CORS issues are handled.

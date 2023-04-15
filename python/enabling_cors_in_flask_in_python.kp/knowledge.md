---
title: What are the steps for enabling cors in flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Add the `Flask-CORS` extension and use it to enable CORS in your Flask app.
---

**Contents**

[TOC]

## Overview

CORS, or Cross-Origin Resource Sharing, is a security feature that restricts web browsers from making requests to a different domain than the one serving the web page. By default, web browsers do not allow scripts to access resources on a different domain than the one serving the web page. In essence, it is a mechanism that allows web servers to tell web browsers whether or not they should allow requests from other origins.

In this tutorial, we will show you how you can enable CORS in Flask using some simple steps.

## Step 1: Install Flask-CORS

The first step is to install the Flask-CORS extension to your Flask application. It can be installed using the following pip command:

```
pip install flask-cors
```

## Step 2: Configure CORS

Once you have installed the Flask-CORS extension, you can now configure it in your Flask application. You can do this by importing the extension and then passing it to the app object. Here is an example:

``` python
from flask import Flask
from flask_cors import CORS

app = Flask(__name__)
CORS(app)
```

This will enable CORS for your entire Flask application. You can also pass in custom configurations to the `CORS` constructor to configure it as per your requirements. For example, if you want to allow all origins, you can do this:

``` python
from flask import Flask
from flask_cors import CORS

app = Flask(__name__)
CORS(app, resources={r"/*": {"origins": "*"}})
```

## Step 3: Test CORS

Once you have enabled CORS in your Flask application, you can now test it by requesting resources from different domains. If CORS has been configured correctly, you should be able to make requests to other domains.

```python
from flask import Flask

app = Flask(__name__)

@app.route('/', methods=['GET'])
def index():
    return "Flask CORS Enabled!"

if __name__ == '__main__':
    app.run()
```

Running the app in on an alternative port and from file (e.g. `app.py`) or command (`python yourfilename.py`) with Flask-CORS integration, you can test an API call to the server URL below - this should work:


https://server_url:5000/


## Conclusion

Cross-Origin Resource Sharing is an essential security feature for web applications that receive requests from multiple domains. In this tutorial, you have learned how to enable CORS in Flask using the Flask-CORS extension in just a few simple steps. By following these steps, you can ensure that your Flask application is secure and can receive requests from other domains.

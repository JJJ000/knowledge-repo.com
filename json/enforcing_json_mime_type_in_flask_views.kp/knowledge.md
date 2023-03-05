---
title: Enforcing the application/json mime type within a flask view
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can force the application/json MIME type in a Flask view by setting the response headers with the .jsonify() method.
---

**Contents**

[TOC]

Using Response Content-Type header

One way to force the application/json MIME type in a Flask view is to manually set the Content-Type header of the response object returned by the view to "application/json". This can be done using the `make_response()` function provided by Flask. Here's an example:

```python
from flask import Flask, make_response, jsonify

app = Flask(__name__)

@app.route('/json')
def json_view():
    # create a Python dictionary to be returned as JSON
    data = {'name': 'John', 'age': 30}

    # create a JSON response object
    resp = make_response(jsonify(data))

    # set the Content-Type header to application/json
    resp.headers['Content-Type'] = 'application/json'

    return resp
```

Using Response class with JSON Encoder

Another way to force the application/json MIME type in a Flask view is to use the `Response` class provided by Flask. The `Response` class allows us to set the Content-Type header and also use a custom JSON encoder to serialize Python objects to JSON. Here's an example:

```python
from flask import Flask, Response
import json

app = Flask(__name__)

class CustomJSONEncoder(json.JSONEncoder):
    def default(self, obj):
        if isinstance(obj, set):
            return list(obj)
        return super().default(obj)

@app.route('/json')
def json_view():
    # create a Python dictionary to be returned as JSON
    data = {'name': 'John', 'age': 30}

    # serialize Python dictionary to JSON using custom JSON encoder
    json_data = json.dumps(data, cls=CustomJSONEncoder)

    # create a JSON response object with Content-Type header set to application/json
    resp = Response(json_data, status=200, mimetype='application/json')

    return resp
```

Using Flask-JSON extension

Flask also provides a third-party extension called Flask-JSON that makes it easier to work with JSON in Flask applications. The Flask-JSON extension provides a `jsonify()` function that automatically sets the Content-Type header to application/json and serializes Python objects to JSON using a custom JSON encoder. Here's an example:

```python
from flask import Flask
from flask_json import FlaskJSON

app = Flask(__name__)
json = FlaskJSON(app)

@app.route('/json')
def json_view():
    # create a Python dictionary to be returned as JSON
    data = {'name': 'John', 'age': 30}

    # return a JSON response using jsonify()
    return json.jsonify(data)
```

Using Flask-Restful extension

If you are building a RESTful API with Flask, you can use the Flask-Restful extension to make it easier to build resource-based endpoints. The `Resource` class provided by Flask-Restful automatically converts Python objects to JSON and sets the Content-Type header to application/json. Here's an example:

```python
from flask import Flask
from flask_restful import Api, Resource

app = Flask(__name__)
api = Api(app)

class JSONView(Resource):
    def get(self):
        # create a Python dictionary to be returned as JSON
        data = {'name': 'John', 'age': 30}

        # return the Python dictionary as a JSON response
        return data

api.add_resource(JSONView, '/json')
```

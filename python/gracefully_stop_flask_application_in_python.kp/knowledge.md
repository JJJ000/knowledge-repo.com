---
title: What are alternative methods to end a flask application without relying on the ctrl-c shortcut?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Call the `shutdown` method of the Flask application object.
---

**Contents**

[TOC]

# How to Stop Flask Application Without Using Ctrl-C in Python?

When you start a Flask application, it runs on a local server as a background process. To stop the server, you can use the following methods:

## Method 1: Using a `shutdown` Endpoint

Flask provides a built-in endpoint that you can use to stop the server programmatically. You can define a route that calls the `shutdown` method, which will stop the server when it receives a `POST` request.

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/shutdown', methods=['POST'])
def shutdown():
    func = request.environ.get('werkzeug.server.shutdown')
    if func is None:
        raise RuntimeError('Not running with the Werkzeug Server')
    func()
    return 'Server shutting down...'

if __name__ == '__main__':
    app.run()
```

In the above example, we define a route called `/shutdown` that takes a `POST` request. The `shutdown` function then calls the `werkzeug.server.shutdown` method to stop the server.

To stop the server, you can send a `POST` request to the `/shutdown` endpoint using the `requests` library:

```python
import requests

response = requests.post('http://localhost:5000/shutdown')
print(response.text)
```

When you run this code, Flask will stop the server and print the message `'Server shutting down...'`.


## Method 2: Using a Signal Handler

If you want to stop the server programmatically from another process or thread, you can define a signal handler. A signal handler is a function that is called when a signal is received by the process.

Here's an example of how to use a signal handler to stop a Flask server:

```python
import signal
from flask import Flask

app = Flask(__name__)

def shutdown_server(signum, frame):
    print('Shutting down server...')
    func = request.environ.get('werkzeug.server.shutdown')
    if func is not None:
        func()

@app.route('/')
def index():
    return 'Hello, World!'

if __name__ == '__main__':
    signal.signal(signal.SIGINT, shutdown_server)
    app.run()
```

In this example, we define a function called `shutdown_server` that stops the server when it receives a `SIGINT` signal (which is sent when you press `Ctrl-C` in the terminal).

We then register this function as the `SIGINT` signal handler using the `signal.signal` method. Finally, we start the Flask server with the `app.run` method.

When you run this code, Flask will start the server and wait for a `SIGINT` signal to stop it. To stop the server, you can send a `SIGINT` signal to the process by pressing `Ctrl-C` in the terminal.

## Conclusion

In summary, there are two ways to stop a Flask server programmatically: by defining a `shutdown` endpoint that calls the `werkzeug.server.shutdown` method, or by defining a signal handler that stops the server when it receives a signal. Both methods allow you to stop the server without using `Ctrl-C` in the terminal.

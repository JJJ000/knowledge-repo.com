---
title: What is the method to send images as a response in flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can use the `send\_file` method from Flask`s `send\_file` module to return images in Flask response in Python.
---

**Contents**

[TOC]

**Section 1: Introduction**

In Flask, we can return images in the response object as either a string or a raw binary buffer. In this tutorial, we will discuss how to return images in Flask response by following simple steps.


**Section 2: Setting up Flask app**

To set up a basic Flask application we need to install Flask and for that, we can use the pip installer. In the terminal simply type this following command:

```
pip install flask
```

**Section 3: Serving images in Flask app**

The first step is to import the necessary module from Flask:

```python
from flask import Flask, send_file, send_from_directory
```

Next, view function is created to serve the image file:

```python
@app.route('/image')
def image():
    filename = 'sample.png'
    return send_file(filename, mimetype='image/png')
```

The `send_file` function takes the filename of the image we want to serve as the argument. The `mimetype` parameter is set to `image/png`. This tells the browser what type of file it is receiving.

**Section 4: Serving images from URL**

Alternatively, we can serve images from a URL as well. We can use the `send_from_directory()` function for this:

```python
@app.route('/<path:filename>')
def serve_static(filename):
    root_dir = os.getcwd()
    return send_from_directory(os.path.join(root_dir, 'static'), filename)
```

In this example, we are serving images from the `static` folder in our app's directory. Any image file in this folder can now be accessed by appending its filename to the URL.

That's it! We now know how to return images in Flask response in Python.

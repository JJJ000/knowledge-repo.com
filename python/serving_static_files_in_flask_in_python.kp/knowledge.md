---
title: What is the best way to deliver static files in flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Flask can serve static files directly from a directory specified in the app.config using the `static\_folder` parameter.
---

**Contents**

[TOC]

# Section 1: Importing the Needed Modules

The first step in serving static files in Flask is to import the necessary modules. This includes the `Flask` module, as well as the `send_from_directory` module from the `werkzeug` package.

```
from flask import Flask
from werkzeug.utils import send_from_directory
```

# Section 2: Defining the Static Directory

Next, you need to define the directory in which your static files are stored. This is done by setting the `static_folder` parameter in the Flask application.

```
app = Flask(__name__, static_folder="static")
```

# Section 3: Setting the Route

The next step is to define a route for serving the static files. This is done with the `@app.route()` decorator.

```
@app.route("/static/<path:filename>")
def serve_static(filename):
    return send_from_directory(app.static_folder, filename)
```

# Section 4: Running the Application

Finally, you need to run the application in order to serve the static files. This is done with the `app.run()` method.

```
if __name__ == "__main__":
    app.run()
```

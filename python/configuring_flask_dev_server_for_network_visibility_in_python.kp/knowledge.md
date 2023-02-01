---
title: Set up flask development server to be accessible on other devices on the same network
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Set the host parameter in the app.run() method to `0.0.0.0` to make the Flask dev server visible across the network.
---

**Contents**

[TOC]

# Section 1: Configure Flask
1. Install Flask: 
```
pip install Flask
```
2. Create a Flask application:
```
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(debug=True)
```

# Section 2: Set Host
1. Set the host parameter to 0.0.0.0:
```
if __name__ == '__main__':
    app.run(host='0.0.0.0', debug=True)
```

# Section 3: Set Port
1. Set the port parameter to the desired port:
```
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000, debug=True)
```

# Section 4: Run Server
1. Run the server:
```
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000, debug=True)
```
2. The server should now be visible across the network.

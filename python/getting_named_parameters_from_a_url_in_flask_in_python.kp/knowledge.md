---
title: What is the best way to access the named parameters from a url using flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the request.args.get() method to get the named parameters from a URL in Flask.
---

**Contents**

[TOC]

1. Importing Flask

```python
from flask import Flask
```

2. Defining the Route

```python
@app.route("/<parameter_name>")
```

3. Accessing the Named Parameter

```python
def get_parameter(parameter_name):
    return parameter_name
```

4. Retrieving the Value

```python
parameter_value = request.args.get('parameter_name')
```

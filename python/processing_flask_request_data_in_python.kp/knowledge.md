---
title: Retrieve the information sent in a flask request
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: The data received in a Flask request can be accessed using the request.form or request.args attributes.
---

**Contents**

[TOC]

### Request Object

The `request` object in Flask contains all the information about the request sent to the server. This includes the headers, form data, arguments, and other data associated with the request. The `request` object is a global variable that is available to all routes and templates in the application.

### Accessing the Data

The data sent in the request can be accessed using the `request` object. The `args` attribute of the `request` object is a dictionary that contains the URL parameters (also known as query string parameters). The `form` attribute is a dictionary that contains the form data submitted in the request. The `headers` attribute is a dictionary that contains the HTTP headers sent in the request.

### Example

For example, if a client sends a request to `/users` with the query string parameter `name=John`, the data can be accessed as follows:

```python
name = request.args.get('name') # John
```

If the client sends a request to `/users` with a form field `age=20`, the data can be accessed as follows:

```python
age = request.form.get('age') # 20
```

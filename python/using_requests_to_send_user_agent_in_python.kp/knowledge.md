---
title: Using the requests library in python, sending a "user-agent" request
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can send a `User-agent` header using the Requests library in Python by specifying the `headers` parameter in the request method.
---

**Contents**

[TOC]

## Section 1 - Importing the Requests Library

To send a "User-agent" using the Requests library in Python, the Requests library must first be imported. This is done by using the following code:

```python
import requests
```

## Section 2 - Setting the User-agent

Next, the User-agent header must be set. This is done by creating a dictionary containing the headers and their values. In this case, the User-agent header is set to a custom value.

```python
headers = {'User-agent': 'MyCustomUserAgent'}
```

## Section 3 - Making the Request

Finally, the request is made using the `requests.get()` function, passing in the URL and the headers dictionary.

```python
response = requests.get('http://example.com', headers=headers)
```

## Section 4 - Verifying the User-agent

To verify that the User-agent was sent correctly, the response headers can be checked. This is done by accessing the `response.headers` dictionary.

```python
user_agent = response.headers['User-agent']
```

The value of the `user_agent` variable should be the same as the one set in the headers dictionary.

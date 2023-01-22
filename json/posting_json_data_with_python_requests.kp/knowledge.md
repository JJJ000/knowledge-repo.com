---
title: What is the syntax for sending a JSON object using Python requests?
authors:
- cool_wizard
tags:
- json
- python
- knowledge
thumbnail: images/json.png
created_at: 2023-01-22 00:00:00
updated_at: 2023-01-22 00:00:00
tldr: To POST JSON data with Python requests, use the `json` parameter of the request method.
---

**Contents**

[TOC]

### Install Requests Library

The first step is to install the [Requests](https://pypi.org/project/requests/) library. This library allows you to make HTTP requests in Python.

### Create Payload

The next step is to create the payload, which is the data you want to send. The payload can be in the form of a dictionary, a list, or a JSON string. 

### Make the Request

Once the payload is created, you can make the request using the Requests library. The following code shows an example of how to make a POST request using the Requests library:

```python
import requests

url = 'http://example.com/api/'

payload = {'key1': 'value1', 'key2': 'value2'}

r = requests.post(url, json=payload)
```

### Check the Response

Finally, you can check the response to see if the request was successful. The following code shows an example of how to check the response:

```python
if r.status_code == 200:
    print('Success!')
else:
    print('An error occurred.')
```

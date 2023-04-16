---
title: What is the process for sending JSON data using Python requests?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Send a dictionary to the post method of the requests module and set the content type to `application/json`.
---

**Contents**

[TOC]

**Section 1: Install the Requests Library**

The Requests library is a popular Python library that can be used to make HTTP requests. To install the Requests library, use the following command:

`pip install requests`

**Section 2: Create the JSON Data**

To POST JSON data with Python Requests, you need to create the JSON data first. This can be done using the json module. For example, the following code creates a JSON object with two keys and values:

```
import json

data = {
    'key1': 'value1',
    'key2': 'value2'
}

json_data = json.dumps(data)
```

**Section 3: Make the POST Request**

Once the JSON data has been created, you can make the POST request using the Requests library. The following code shows an example of how to do this:

```
import requests

url = 'http://example.com/api/endpoint'

response = requests.post(url, json=json_data)
```

**Section 4: Check the Response**

Finally, you can check the response from the POST request to make sure it was successful. The following code shows an example of how to do this:

```
if response.status_code == 200:
    print('Success!')
else:
    print('Error!')
```

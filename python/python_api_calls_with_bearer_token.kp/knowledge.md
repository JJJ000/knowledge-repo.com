---
title: Executing a Python API request while utilizing an API that mandates a bearer token
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To make an API call in Python with an API that requires a bearer token, you can add the token to the headers of the HTTP request using the `Authorization` key.
---

**Contents**

[TOC]

## Obtaining the Bearer Token

The first step in making an API call with a bearer token is to obtain the token. This process will vary depending on the API being used, but generally involves authenticating with the API provider and generating a token that can be used to authenticate future requests. Once you have obtained the token, it should be stored securely, such as in an environment variable or configuration file.

## Adding the Bearer Token to the Request

The next step is to add the bearer token to the request headers. This is typically done by setting an Authorization header with the value "Bearer {token}", where {token} is the actual token value. Here is an example of how to add the bearer token to a request using the requests library in Python:

```
import requests

url = "https://api.example.com/some-endpoint"

headers = {
    "Authorization": "Bearer my_api_token"
}

response = requests.get(url, headers=headers)

print(response.json())
```

In this example, we are making a GET request to the endpoint https://api.example.com/some-endpoint, and including the bearer token "my_api_token" in the Authorization header.

## Handling Authentication Errors

If the bearer token is invalid or has expired, the API server will typically respond with a 401 Unauthorized error. To handle this error in your Python code, you can check the status code of the response and either try generating a new token or alerting the user that their credentials are invalid. Here is an example of how to handle authentication errors in the requests library:

```
import requests

url = "https://api.example.com/some-endpoint"

headers = {
    "Authorization": "Bearer my_api_token"
}

response = requests.get(url, headers=headers)

if response.status_code == 401:
    # Handle authentication error
    print("Invalid API token")
else:
    # Handle successful response
    print(response.json())
```

In this example, we are checking the status code of the response and printing an error message if the code is 401 (Unauthorized). Otherwise, we are printing the response json.

---
title: Send both a JSON and file in a single request using Python requests
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Yes, it is possible to post JSON and file in a single request in JSON format using the Requests library.
---

**Contents**

[TOC]

1. Overview

The Python Requests library allows for sending requests to web servers with data in the JSON format. It also allows for sending files in the same request. This article will explain how to send both JSON and a file in a single request using the Python Requests library.

2. Prerequisites

Before getting started, it is important to make sure that the Python Requests library is installed. This can be done using the pip package manager with the following command:

`pip install requests`

3. Sending JSON and File in Single Request

Once the Python Requests library is installed, sending JSON and a file in a single request is relatively straightforward. The following code snippet shows an example of how to do this:

```
import requests

url = 'http://example.com/upload'

data = {
    'key1': 'value1',
    'key2': 'value2'
}

files = {
    'file': open('/path/to/file', 'rb')
}

r = requests.post(url, data=data, files=files)
```

In the above code snippet, the `data` variable contains the JSON data that will be sent in the request. The `files` variable contains the file that will be sent in the request. Finally, the `requests.post()` method is used to send the request with the JSON data and file.

4. Conclusion

In this article, we have seen how to send both JSON and a file in a single request using the Python Requests library. This is a useful technique to know when sending data to web servers.

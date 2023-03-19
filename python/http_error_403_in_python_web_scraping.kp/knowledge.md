---
title: How to overcome the http error 403 encountered while conducting web scraping in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: HTTP error 403 in Python 3 Web Scraping means that the server is denying access to the requested resource due to authentication or authorization failure.
---

**Contents**

[TOC]

Section 1: Introduction to HTTP error 403
HTTP error 403 is an HTTP status code indicating that the client or user is not authorized to access the requested resource. This error is often encountered during web scraping, which involves extracting data from websites using software tools or scripts. HTTP 403 error can be encountered due to various reasons such as authentication issues, incorrect permissions, server-side configurations, etc.

Section 2: Solutions to HTTP error 403 in Python 3 Web Scraping
1. User-Agent Header: Some websites block web scraping bots or scripts that do not provide a valid User-Agent header. Hence, adding a user-agent header to your web scraping script can solve the HTTP 403 error in Python 3 Web Scraping.

Example code snippet for adding user-agent header:

```
import requests

headers = {
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.36'
}

response = requests.get('https://www.example.com', headers=headers)

print(response.content)
```

2. Cookies: Websites that require authentication or permission may also use cookies to track user sessions. In such cases, it is necessary to include the appropriate cookies in your web scraping script to avoid the HTTP 403 error.

Example code snippet for adding cookies:

```
import requests

cookies = {
    'sessionid': '1234'
}

response = requests.get('https://www.example.com', cookies=cookies)

print(response.content)
```

3. Proxies: Some websites may block requests from a particular IP address or location. In such cases, using a proxy server can help bypass these restrictions and prevent the HTTP 403 error.

Example code snippet for using proxies:

```
import requests

proxies = {
    'http': 'http://yourproxyaddress:port',
    'https': 'https://yourproxyaddress:port'
}

response = requests.get('https://www.example.com', proxies=proxies)

print(response.content)
```

Section 3: Summary
HTTP error 403 is a common error encountered during web scraping in Python 3. It indicates that the user or client is not authorized to access the requested resource. Adding a valid User-Agent header, appropriate cookies, or using a proxy server can help resolve the HTTP 403 error and allow for successful web scraping.

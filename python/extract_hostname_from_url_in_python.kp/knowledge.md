---
title: Retrieve the protocol and hostname from a given url
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use urlparse library in Python to get the protocol and host name from a URL.
---

**Contents**

[TOC]

## Section 1: Understanding the Problem

We have a URL, and we want to extract the protocol and the hostname from it. This is a relatively simple problem, but we need to make sure that we handle different types of URLs, including those that use various protocols such as "http", "https", "ftp", etc.

## Section 2: Parsing the URL

To extract the protocol and the hostname from a URL, we can use the `urlparse` function from the `urllib` library. This function breaks down a URL into its component parts and returns a `ParseResult` object.

Here is an example of how to use `urlparse` to extract the protocol and the hostname from a URL:

```python
from urllib.parse import urlparse

url = "https://www.example.com/path/to/file.html"
parsed_url = urlparse(url)

print(parsed_url.scheme)    # output: "https"
print(parsed_url.netloc)    # output: "www.example.com"
```

In this example, `urlparse` takes in the URL `https://www.example.com/path/to/file.html` and returns a `ParseResult` object. We can then access the scheme (protocol) with `parsed_url.scheme` and the hostname with `parsed_url.netloc`.


## Section 3: Handling Invalid URLs

It's worth noting that if a URL is invalid, `urlparse` may not be able to extract the components we need. In such cases, we should handle the `ValueError` exception that may be raised by `urlparse`.

Here is an example of how to handle exceptions when using `urlparse`:

```python
from urllib.parse import urlparse

url = "invalid-url"
try:
    parsed_url = urlparse(url)
    print(parsed_url.scheme)
    print(parsed_url.netloc)
except ValueError as e:
    print(f"Error parsing URL: {e}")
```

In this example, `urlparse` will raise a `ValueError` exception because `url` is an invalid URL. We handle the exception by printing an error message.

## Section 4: Conclusion

In this solution, we have shown how to extract the protocol and the hostname from a URL using the `urlparse` function from the `urllib` library. We have also demonstrated how to handle exceptions when parsing invalid URLs. Overall, this is a simple and reliable way to extract the parts of a URL that we need.

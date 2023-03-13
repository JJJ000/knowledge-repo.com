---
title: Convert url query parameters into a Python dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: In Python, you can use the built-in module urllib.parse.parse\_qs to convert a URL`s query parameters to a dictionary.
---

**Contents**

[TOC]

Converting URL query parameters to dictionary in Python

One common task when working with HTTP/HTTPS requests is handling query parameters. These parameters are values passed in the URL in the form of key-value pairs. When dealing with these values, it can be useful to convert them to a dictionary. Python offers a simple and effective way to do this using the urllib.parse module.

1. Parsing Query Parameters

The first step to converting query parameters to a dictionary is to parse the URL. This can be done using the urlparse function from the urllib.parse module. This function will split the URL into several parts: scheme, netloc, path, params, query and fragment.

Here is an example of how to parse a URL:

```python
from urllib.parse import urlparse

url = 'https://example.com/search?q=query+parameters&sort=price'
parsed_url = urlparse(url)

print(parsed_url)
```

Output:

```
ParseResult(scheme='https', netloc='example.com', path='/search', params='', query='q=query+parameters&sort=price', fragment='')
```

Notice that the query parameter is present in the result.

2. Converting Query Parameters to Dictionary

Once the URL has been parsed, we can convert the query parameters to a dictionary using the parse_qs function from the same module.

```python
from urllib.parse import urlparse, parse_qs

url = 'https://example.com/search?q=query+parameters&sort=price'
parsed_url = urlparse(url)

params_dict = parse_qs(parsed_url.query)
print(params_dict)
```

Output:

```
{'q': ['query parameters'], 'sort': ['price']}
```

The parse_qs function returns a dictionary where each key is a query parameter and its value is a list with all the values passed for that parameter.

3. Handling Duplicated Parameters

It may happen that a query parameter is passed more than once, in this case parse_qs will return a dictionary with lists with more than one value.

```python
from urllib.parse import urlparse, parse_qs

url = 'https://example.com/search?q=query+parameters&sort=price&q=python'
parsed_url = urlparse(url)

params_dict = parse_qs(parsed_url.query)
print(params_dict)
```

Output:

```
{'q': ['query parameters', 'python'], 'sort': ['price']}
```

To handle this case, we can use the get function from the dictionary object and then store a list with all the parameters values.

```python
from urllib.parse import urlparse, parse_qs

url = 'https://example.com/search?q=query+parameters&sort=price&q=python'
parsed_url = urlparse(url)

params_dict = {}
for k, v in parse_qs(parsed_url.query).items():
    params_dict.setdefault(k, []).extend(v)

print(params_dict)
```

Output:

```
{'q': ['query parameters', 'python'], 'sort': ['price']}
```

Now the dictionary contains all the query parameters, including the duplicated ones.

4. Conclusion

Converting URL query parameters to a dictionary is a simple task that can be very useful when handling HTTP/HTTPS requests. By using the urllib.parse module, we can parse the URL and convert the query parameters to a dictionary with just a few lines of code.

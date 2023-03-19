---
title: What are the steps for combining absolute and relative urls?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `urljoin` function from the `urllib.parse` module in Python to join absolute and relative URLs.
---

**Contents**

[TOC]

## Introduction

In Python, we can join two URLs, where one is an absolute URL and the other one is a relative URL. The process of joining them is called URL concatenation, and it's a common task for web development.

In this article, we'll discuss the different ways to join absolute and relative URLs in Python. We'll also provide examples for each section to make it easier to follow.

## Using urlparse.urljoin()

The `urljoin()` method from the `urlparse` module can be used to join two URLs. This method has the advantage of taking care of the relative URL and avoiding duplicates. Here's an example:

```python
from urllib.parse import urljoin

url1 = "https://www.example.com"
url2 = "/blog"
url3 = urljoin(url1, url2)

print(url3)
```

Output:
```
https://www.example.com/blog
```

In this example, we're using the `urlparse.urljoin()` method to join `url1` (an absolute URL) and `url2` (a relative URL) into `url3`. The method takes care of the relative URL and returns the correct result.

## Using f-strings

We can also concatenate URLs using f-strings. This method is less recommended since it doesn't take care of the relative URL nor eliminates duplicates. However, it's a quick option for joining URLs. Here's how:

```python
relative_url = "/blog"
absolute_url = "https://www.example.com"

new_url = f"{absolute_url}{relative_url}"

print(new_url)
```

Output:
```
https://www.example.com/blog
```

In this example, we're using f-strings to concatenate `absolute_url` and `relative_url` into `new_url`.

## Using format()

Another option is to use the `format()` method to concatenate URLs. This method is similar to f-strings in that it doesn't take care of the relative URL nor eliminates duplicates. Here's how:

```python
relative_url = "/blog"
absolute_url = "https://www.example.com"

new_url = "{}{}".format(absolute_url, relative_url)

print(new_url)
```

Output:
```
https://www.example.com/blog
```

In this example, we're using the `format()` method to concatenate `absolute_url` and `relative_url` into `new_url`.

## Conclusion

In this article, we discussed different ways of joining absolute and relative URLs in Python: using the `urlparse.urljoin()` method, f-strings, and the `format()` method. While `urljoin()` is the recommended method since it takes care of the relative URL, f-strings and `format()` are also options for quick URL concatenation.

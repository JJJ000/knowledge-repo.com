---
title: What is the process for executing html encoding/decoding with python/django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the built-in `html` module in Python for HTML decoding/encoding `import html; encoded\_string = html.escape(unencoded\_string)` and `decoded\_string = html.unescape(encoded\_string)`. For Django, use the `django.utils.html` module `import django.utils.html; encoded\_string = django.utils.html.escape(unencoded\_string)` and `decoded\_string = django.utils.html.unescape(encoded\_string)`.
---

**Contents**

[TOC]

## Introduction

Python and Django provide several methods for HTML decoding/encoding. HTML decoding is a process of converting HTML entities into their corresponding characters. HTML encoding is the opposite process of converting characters into their HTML entity representations. In this article, we will discuss the different methods for HTML decoding/encoding in Python/Django.

## Using html.parser module

The html.parser module in Python can be used to decode HTML entities. The following code demonstrates how to use the html.parser module to decode HTML entities:

```python
import html.parser as htmlparser
string_with_entities = "I&apos;m a string with &nbsp; &ndash; entities"
decoded_string = htmlparser.HTMLParser().unescape(string_with_entities)
print(decoded_string)
```

Output:
```
I'm a string with   – entities
```

Similarly, to encode HTML entities, we can use the `escape` method of the `html.parser` module:

```python
import html.parser as htmlparser
string_to_encode = "I'm a string with non-ASCII characters like àéîöù"
encoded_string = htmlparser.HTMLParser().escape(string_to_encode)
print(encoded_string)
```

Output:
```
I'm a string with non-ASCII characters like &agrave;&eacute;&icirc;&ouml;&ugrave;
```

## Using html module

The html module in Python can also be used for HTML decoding/encoding. The following code demonstrates how to decode HTML entities using the html module:

```python
import html
string_with_entities = "I&apos;m a string with &nbsp; &ndash; entities"
decoded_string = html.unescape(string_with_entities)
print(decoded_string)
```

Output:
```
I'm a string with   – entities
```

Similarly, to encode HTML entities, we can use the `escape` method of the `html` module:

```python
import html
string_to_encode = "I'm a string with non-ASCII characters like àéîöù"
encoded_string = html.escape(string_to_encode)
print(encoded_string)
```

Output:
```
I'm a string with non-ASCII characters like &agrave;&eacute;&icirc;&ouml;&ugrave;
```

## Using Django template tag

Django provides a template tag to encode HTML entities. The `escape` template tag can be used to encode HTML entities in Django templates. In the following example, the `escape` template tag is used to encode a variable `my_var`:

```html
{% load humanize %}

{{ my_var|escape }}
```

Similarly, to decode HTML entities in a Django template, we can use the `safe` filter:

```html
{% autoescape off %}
{{ my_var|safe }}
{% endautoescape %}
```

The `autoescape` tag is used to turn off the automatic HTML escaping in the template. The `safe` filter is used to mark the variable as safe and prevents Django from escaping the HTML entities.

## Conclusion

In this article, we have discussed the different methods for HTML decoding/encoding in Python/Django. The html.parser module and the html module can be used for HTML decoding/encoding in Python. Django provides a template tag `escape` to encode HTML entities and the `safe` filter to decode HTML entities in Django templates.

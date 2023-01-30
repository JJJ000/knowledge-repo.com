---
title: What distinctions exist between the urllib, urllib2, urllib3, and requests modules?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The urllib, urllib2, and urllib3 modules are built-in Python modules for handling HTTP requests, while the requests module is an external library for making HTTP requests easier to handle.
---

**Contents**

[TOC]

### urllib

The urllib module in Python is a collection of modules that allow you to perform a variety of operations on URLs. It includes functions such as urlopen, urlretrieve and urlparse. This module is part of the standard library and is very easy to use.

### urllib2

The urllib2 module is an extension of the urllib module. It provides additional features such as the ability to handle HTTP authentication, redirections, cookies, and more. It also provides an interface for working with HTTP and FTP requests.

### urllib3

urllib3 is an improved version of the urllib and urllib2 modules. It provides support for connection pooling, thread safety, and SSL/TLS. It also provides support for HTTP/2 and proxy handling.

### Requests

The requests module is an alternative to the urllib, urllib2, and urllib3 modules. It is designed to be more user-friendly and provides a simpler interface for making HTTP requests. It also supports many advanced features such as authentication, cookies, and SSL/TLS.

---
title: Using python's standard library to locate local ip addresses
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the socket library to retrieve a list of local IP addresses.
---

**Contents**

[TOC]

**Section 1: Using the socket Library**

The socket library in Python allows us to retrieve the local IP address of the system. By using the gethostname() and gethostbyname() functions, we can retrieve the local IP address of the system.

The gethostname() function returns the hostname of the system and the gethostbyname() function returns the IP address associated with that hostname.

**Section 2: Using the netifaces Library**

The netifaces library in Python allows us to retrieve the local IP address of the system. This library provides an interface to the underlying operating system to retrieve the IP address associated with a particular interface.

The ifaddresses() function in this library returns a dictionary containing the IP addresses associated with each interface. We can then use this dictionary to retrieve the local IP address of the system.

**Section 3: Using the ipaddress Library**

The ipaddress library in Python allows us to retrieve the local IP address of the system. This library provides an interface to the underlying operating system to retrieve the IP address associated with a particular interface.

The IPv4Address() function in this library returns an IP address object that contains the local IP address of the system. We can then use this object to retrieve the local IP address of the system.

**Section 4: Using the platform Library**

The platform library in Python allows us to retrieve the local IP address of the system. This library provides an interface to the underlying operating system to retrieve the IP address associated with a particular interface.

The node() function in this library returns the hostname of the system. We can then use the gethostbyname() function to retrieve the IP address associated with that hostname. This IP address is the local IP address of the system.

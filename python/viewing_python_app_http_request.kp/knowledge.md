---
title: What is the complete http request being sent by my Python application?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can view the entire HTTP request by using the `requests` library`s `request.get` or `request.post` methods.
---

**Contents**

[TOC]

1. Using a Network Monitor 
   - Install a network monitor such as Wireshark or Fiddler. 
   - Configure the network monitor to capture the traffic from the Python application.
   - Inspect the traffic to view the HTTP requests.

2. Using Python Libraries 
   - Use a library such as the requests library to send the HTTP request. 
   - Inspect the request object to view the entire HTTP request.
   - Use the request.headers and request.data attributes to view the request headers and body.

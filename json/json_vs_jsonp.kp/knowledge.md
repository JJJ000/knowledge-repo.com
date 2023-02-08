---
title: How do JSON and jsonp differ?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: JSON is a data-interchange format, while JSONP is a technique used to bypass the same-origin policy and allow data to be requested from other domains.
---

**Contents**

[TOC]

# JSON
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays. It is used to transmit data between a server and a web application.

# JSONP
JSONP (JSON with Padding) is a technique used by web developers to overcome the cross-domain restrictions imposed by the same-origin policy. It is a method of sending data from a server to a web page, by using a <script> tag with a URL that contains the JSON data.

# Differences
1. JSON is used to transmit data between a server and a web application, while JSONP is used to overcome the cross-domain restrictions imposed by the same-origin policy. 
2. JSON is a text-based, human-readable format for representing simple data structures and associative arrays, while JSONP uses a <script> tag with a URL that contains the JSON data. 
3. JSON is a lightweight data-interchange format, while JSONP is a technique used by web developers. 
4. JSON does not support callback functions, while JSONP does.

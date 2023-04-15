---
title: Is there a full list of http response codes available in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, Java does not have a complete enum for HTTP response codes.
---

**Contents**

[TOC]

### What is an Enum?
Enums are a type of data type in Java that allow the programmer to define a set of named constants. Enums are used to represent a group of related values and can be used to assign meaningful names to sets of numeric values. 

### Does Java have a Complete Enum for HTTP Response Codes?
Yes, Java does have a complete enum for HTTP response codes. The enum is defined in the `HttpServletResponse` class in the `javax.servlet.http` package. The enum contains all of the standard HTTP response codes, such as `200 OK`, `404 Not Found`, `301 Moved Permanently`, etc. 

### How to Use the Enum
The enum can be used to check the status code of an HTTP response. For example, if a web application receives an HTTP response with a status code of `404 Not Found`, the application could check the enum to determine what the status code means.

### Benefits of Using the Enum
Using the enum makes it easier to work with HTTP response codes. It eliminates the need to manually look up the meaning of each code and allows the programmer to quickly determine the meaning of a response code. Additionally, using the enum ensures that the application is using the correct codes, as the enum contains all of the standard HTTP response codes.

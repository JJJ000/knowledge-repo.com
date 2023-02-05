---
title: Construct a url using an httpservletrequest
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the HttpServletRequest.getRequestURL() method to get the complete URL in Java.
---

**Contents**

[TOC]

##### Section 1: Overview
HttpServletRequest is an interface in the Java Servlet API which is used to represent a request made by a client to a server. The interface contains methods to get information such as the request type, parameters, headers, and attributes. It also provides methods to complete a URL by adding a query string, path info, and context path. 

##### Section 2: Methods
The methods used to complete a URL in the HttpServletRequest interface are as follows: 
- getContextPath(): This method returns the context path of the servlet. 
- getPathInfo(): This method returns the path information associated with the request. 
- getQueryString(): This method returns the query string associated with the request. 

##### Section 3: Example
The following example demonstrates how to use the methods of the HttpServletRequest interface to complete a URL: 
```
String contextPath = request.getContextPath();
String pathInfo = request.getPathInfo();
String queryString = request.getQueryString();

String completeURL = contextPath + pathInfo + "?" + queryString;
```

##### Section 4: Conclusion
The HttpServletRequest interface provides methods to complete a URL by adding a query string, path info, and context path. This is useful when a client makes a request to a server and the server needs to generate a complete URL in order to respond to the request.

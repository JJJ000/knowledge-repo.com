---
title: What is the process for sending an http request in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the HttpURLConnection class to send HTTP requests in Java.
---

**Contents**

[TOC]

### Using the URL Class
The URL class can be used to send an HTTP request in Java. The URL class is part of the java.net package and can be used to represent a URL address. 

### Constructing the URL
The URL class provides a constructor to create a URL object from a String representation of the URL address. This constructor can be used to create a URL object from a valid URL address. 

### Opening the Connection
Once a URL object is created, the openConnection() method can be used to open a connection to the URL represented by the object. This method returns an instance of the URLConnection class, which can be used to send the HTTP request. 

### Sending the Request
The URLConnection class provides the getInputStream() method which can be used to send the HTTP request. This method returns an InputStream object which can be used to read the response of the request.

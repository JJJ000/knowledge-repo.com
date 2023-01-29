---
title: Break down a uri string into a name and value pair
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A URI String can be parsed into a Name-Value Collection in Java using the java.net.URLEncoder class.
---

**Contents**

[TOC]

### Overview

A Uniform Resource Identifier (URI) is a string of characters used to identify a resource on the internet. Parsing a URI string into a name-value collection involves extracting the different components of the URI and mapping them to a set of key-value pairs. This can be done in Java using the java.net.URI class.

### Java.net.URI

The java.net.URI class provides a constructor that takes a URI string as an argument. This constructor parses the string and creates a URI object which contains the various components of the URI. These components can be accessed using the getScheme(), getHost(), getPath(), getQuery(), and getFragment() methods.

### Mapping to a Name-Value Collection

Once the components of the URI have been extracted, they can be mapped to a name-value collection. The query component of the URI can be parsed into a set of key-value pairs using the java.net.URLDecoder class. The other components can be added to the collection as individual values.

### Example

The following example demonstrates how to parse a URI string into a name-value collection in Java.

```java
String uriString = "http://example.com/path?key1=value1&key2=value2#fragment";

URI uri = new URI(uriString);

Map<String, String> params = new HashMap<>();

// Add scheme
params.put("scheme", uri.getScheme());

// Add host
params.put("host", uri.getHost());

// Add path
params.put("path", uri.getPath());

// Parse query into name-value pairs
String query = uri.getQuery();
String[] pairs = query.split("&");
for (String pair : pairs) {
    String[] parts = pair.split("=");
    params.put(URLDecoder.decode(parts[0], "UTF-8"),
               URLDecoder.decode(parts[1], "UTF-8"));
}

// Add fragment
params.put("fragment", uri.getFragment());
```

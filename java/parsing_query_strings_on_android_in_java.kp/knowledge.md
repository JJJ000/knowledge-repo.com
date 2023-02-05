---
title: Analyzing query parameters on an Android device
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Android SDK provides the Uri.getQueryParameter() method for parsing query strings in Java.
---

**Contents**

[TOC]

## Using `Uri`
The `Uri` class provides a convenient way to parse query strings on Android. It can parse a string into a `Uri` object, which can then be used to retrieve the query parameters.

To use `Uri` to parse a query string, first create a `Uri` object using the `parse` method, passing in the query string as a parameter:

```java
Uri uri = Uri.parse(queryString);
```

The query parameters can then be retrieved using the `getQueryParameter` method, passing in the parameter name as a parameter:

```java
String paramValue = uri.getQueryParameter(paramName);
```

## Using `URLEncodedUtils`
The `URLEncodedUtils` class provides a convenient way to parse query strings on Android. It can parse a string into a list of `NameValuePair` objects, which can then be used to retrieve the query parameters.

To use `URLEncodedUtils` to parse a query string, first create a list of `NameValuePair` objects using the `parse` method, passing in the query string as a parameter:

```java
List<NameValuePair> params = URLEncodedUtils.parse(queryString);
```

The query parameters can then be retrieved using the `getParameter` method, passing in the parameter name as a parameter:

```java
String paramValue = URLEncodedUtils.getParameter(params, paramName);
```

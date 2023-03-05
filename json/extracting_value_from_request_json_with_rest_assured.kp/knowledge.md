---
title: Can we get a value from the request JSON with certainty?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: Yes, it is possible to extract values from request JSON using Rest-assured.
---

**Contents**

[TOC]

# Yes, It is Possible

Rest-Assured provides a set of methods to extract values from the request JSON. These methods allow developers to get values from the response body and use them in their tests.

## Extracting Values from the Response Body

The most common way to extract values from the response body is to use the `jsonPath()` method. This method takes a JSON path expression, evaluates it against the response body and returns the matching values.

```java
String value = given().
				when().
					get("/some/path").
				then().
					extract().
					path("$.some.path.in.the.response");
```

## Extracting Values from the Response Headers

The `header()` method can be used to extract values from the response headers. This method takes a header name as an argument and returns the value of the header.

```java
String headerValue = given().
						when().
							get("/some/path").
						then().
							extract().
							header("some-header");
```

## Extracting Values from the Response Cookies

The `cookie()` method can be used to extract values from the response cookies. This method takes a cookie name as an argument and returns the value of the cookie.

```java
String cookieValue = given().
						when().
							get("/some/path").
						then().
							extract().
							cookie("some-cookie");
```

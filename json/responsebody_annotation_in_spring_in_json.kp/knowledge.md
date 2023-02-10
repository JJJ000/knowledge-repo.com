---
title: What is the function of the spring @responsebody annotation?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The @ResponseBody annotation is used to serialize a Java object into JSON and write it to the body of the response.
---

**Contents**

[TOC]

# Overview
The Spring @ResponseBody annotation is used to bind the return value of a controller method to the response body of an HTTP request. When used in conjunction with the Spring MVC framework, the @ResponseBody annotation can be used to return JSON data from a controller method.

# How it Works
The @ResponseBody annotation works by using an HTTP message converter to serialize the return value of the controller method into the response body of the HTTP request. The message converter can be configured to convert the return value into a specific format such as JSON. Once the return value has been serialized, it is written to the response body of the HTTP request.

# Example
For example, consider the following controller method:

```
@ResponseBody
public User getUser(int userId) {
  return userService.getUser(userId);
}
```

In this example, the @ResponseBody annotation is used to serialize the return value of the getUser() method into the response body of the HTTP request. The message converter is configured to convert the return value into a JSON format. The response body of the HTTP request will contain the serialized JSON representation of the User object.

# Conclusion
The Spring @ResponseBody annotation is a powerful tool for returning JSON data from a controller method. It uses an HTTP message converter to serialize the return value of the controller method into the response body of the HTTP request. By using the @ResponseBody annotation, developers can easily return JSON data from their controller methods.

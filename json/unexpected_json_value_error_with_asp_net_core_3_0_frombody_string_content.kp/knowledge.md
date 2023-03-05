---
title: When using [frombody] with ASP.NET core 3.0, if the content is a string, you may receive the error message "the JSON value could not be converted to system.string."
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The content being passed to the controller method as a string is not in a valid JSON format.
---

**Contents**

[TOC]

Section 1: Introduction
ASP.NET Core 3.0 is an open-source, cross-platform framework for building modern, cloud-based, and internet-connected applications. It is a high-performance, modular framework that offers a range of capabilities to developers for building web applications, APIs, and services. In ASP.NET Core 3.0, developers can use the [FromBody] attribute to bind the request body to an action method parameter.

Section 2: Issue with [FromBody] string content 
When using [FromBody] with a string parameter in ASP.NET Core 3.0, the system may return an error message that reads "The JSON value could not be converted to System.String." This error message usually occurs when the content in the request body is not a valid JSON string.

Section 3: Possible Solutions
There are several possible solutions to this issue, depending on the source of the invalid JSON in the request body. One solution is to validate the JSON data on the client side before sending it to the server. Another solution is to use a try-catch block and handle the "JsonReaderException" exception that is thrown when the JSON content is invalid. Additionally, you could try to use a different data type or format for the input data such as using a JSON Object or deserialize the JSON string content into an object.

Section 4: Conclusion
ASP.NET Core 3.0 is a powerful framework for building modern web applications, APIs, and services. When using [FromBody] attribute with string content, developers may encounter an issue where the system returns "The JSON value could not be converted to System.String." However, there are multiple solutions to this problem, depending on the source of the invalid JSON. With the appropriate validation and handling techniques, developers can effectively work with string content in ASP.NET Core 3.0.

---
title: C#'s httpclient does not have a postasjsonasync method
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, HttpClient does not support the PostAsJsonAsync method.
---

**Contents**

[TOC]

1. Overview 
2. PostAsJsonAsync Method
3. Alternatives
4. Conclusion

## Overview
HttpClient is a library in .NET Core that provides a programming interface for modern HTTP applications. It is designed to be used with the .NET Core framework and provides an easy-to-use API for making HTTP requests. HttpClient is used to send and receive data over the internet, and it supports a wide range of HTTP methods, such as GET, POST, PUT, DELETE, and more.

## PostAsJsonAsync Method
HttpClient does not support the PostAsJsonAsync method. This method is used to send a JSON-encoded object to a server, and it is not supported by HttpClient. The only way to send a JSON-encoded object with HttpClient is to use the PostAsync method and manually encode the object as a JSON string.

## Alternatives
There are a few alternatives to HttpClient that do support the PostAsJsonAsync method. These include the RestSharp library and the JSON.NET library. Both of these libraries provide an easy-to-use API for making HTTP requests, and they both support the PostAsJsonAsync method.

## Conclusion
HttpClient does not support the PostAsJsonAsync method. However, there are a few alternatives that do support this method, such as the RestSharp library and the JSON.NET library. These libraries provide an easy-to-use API for making HTTP requests, and they both support the PostAsJsonAsync method.

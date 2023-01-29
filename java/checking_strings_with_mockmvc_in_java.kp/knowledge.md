---
title: Testing a string in the response body using mockmvc
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the MockMvcResultMatchers.content().string(String) method to check if the response body contains the specified String.
---

**Contents**

[TOC]

### Creating the Test

To check a String in the response body using MockMvc, the most straightforward approach is to use the `MockMvcResultMatchers.content()` method. This method takes a `String` argument and will return a `ResultMatcher` that can be used to check the response body.

### Setting up the Test

Before the test can be run, the `MockMvc` instance must be configured with the appropriate `RequestBuilder` and `ResultMatcher` objects. The `RequestBuilder` is used to define the request that will be sent to the MockMvc instance, and the `ResultMatcher` is used to check the response body for the expected String.

### Running the Test

Once the `MockMvc` instance is configured, the test can be run by calling the `MockMvc.perform()` method. This method takes the `RequestBuilder` and `ResultMatcher` objects as arguments, and will execute the request and check the response body for the expected String.

### Asserting the Results

Finally, the results of the test can be asserted by using the `MockMvcResultMatchers.status()` method. This method takes a `HttpStatus` argument and will return a `ResultMatcher` that can be used to check the response status code. If the response status code matches the expected value, then the test has passed.

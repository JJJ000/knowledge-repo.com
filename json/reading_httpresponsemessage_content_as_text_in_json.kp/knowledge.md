---
title: What is the process for extracting the text from an httpresponsemessage?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the ReadAsStringAsync() method to read the HttpResponseMessage content as text in JSON.
---

**Contents**

[TOC]

1. Deserializing the Response Content 
  
  a. Retrieve the response content as a string 
  
    i. Use the `Content` property of the `HttpResponseMessage` to access the response content.
  
    ii. Use the `ReadAsStringAsync()` method to retrieve the content as a string.
  
  b. Deserialize the response content 
  
    i. Use the `DeserializeObject<T>()` method of the `JsonConvert` class to deserialize the response content into a strongly typed object.
  
    ii. Specify the type of object to deserialize the response content into as the generic type parameter.

2. Serializing the Response Content 
  
  a. Retrieve the response content as a string 
  
    i. Use the `Content` property of the `HttpResponseMessage` to access the response content.
  
    ii. Use the `ReadAsStringAsync()` method to retrieve the content as a string.
  
  b. Serialize the response content 
  
    i. Use the `SerializeObject()` method of the `JsonConvert` class to serialize the response content into a JSON string.
  
    ii. Specify the object to serialize as the method parameter.

---
title: Sending JSON parameters using restsharp
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Send a JSON object as the request body by setting the request body directly and setting the request content type to `application/json`.
---

**Contents**

[TOC]

**Section 1 - Introduction**

RESTSharp is a powerful and flexible library for creating RESTful web services. It allows developers to easily create and consume RESTful web services. One of the features of RESTSharp is the ability to post JSON parameters to a server. This is useful for sending complex data structures to a server such as objects, arrays, and nested objects.

**Section 2 - Setting Up the Request**

The first step to posting JSON parameters with RESTSharp is to set up the request. This is done by creating a new RestRequest object and setting the request type to “POST”. Then, the parameters to be sent should be added to the request object.

**Section 3 - Setting the JSON Parameters**

Once the request object has been set up, the JSON parameters should be added to it. This can be done by creating a new JsonObject and adding the desired parameters to it. The parameters should be added in the same way as they would be added to a normal JSON object.

**Section 4 - Sending the Request**

The final step is to send the request to the server. This is done by calling the Execute method of the RestClient object. This method will send the request to the server and return the response. The response can then be parsed and used as needed.

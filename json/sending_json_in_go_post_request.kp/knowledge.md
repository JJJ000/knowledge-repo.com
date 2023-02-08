---
title: What is the syntax for sending a JSON string in a post request using go?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.Marshal() method to encode the JSON string into a byte array, and then use the http.NewRequest() method to create an HTTP request with the byte array as its body.
---

**Contents**

[TOC]

## Preparation

Before sending a JSON string in a POST request, the JSON string must be formatted properly. This can be done using the `json.Marshal` function in Go. This function takes a struct and returns a JSON-encoded byte array.

## Setup

The `http.NewRequest` function can be used to create a new POST request with the JSON string as the body. The `Content-Type` header should be set to `application/json` to indicate that the request body is in JSON format. Additionally, the `http.Client` type can be used to send the request.

## Sending

The `http.Client.Do` method can be used to send the request. This method takes the request as a parameter and returns a `http.Response` type. The response can then be used to check the status code and read the response body.

## Conclusion

To send a JSON string in a POST request in Go, the JSON string must first be formatted properly using `json.Marshal`. The `http.NewRequest` and `http.Client.Do` methods can then be used to create and send the request, respectively. Finally, the response can be used to check the status code and read the response body.

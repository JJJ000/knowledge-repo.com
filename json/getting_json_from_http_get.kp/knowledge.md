---
title: What is the JSON response from an http.get request?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.Unmarshal function to get a JSON response from an http.Get request.
---

**Contents**

[TOC]

1. Make a Request

In order to make a request for a JSON response from an HTTP GET request, you will need to use an HTTP client library. The most popular HTTP client library for Go is the `net/http` package.

2. Set Request Headers

In order to receive a JSON response, you must set the `Accept` header of the request to `application/json`. You can do this by using the `http.Header` type and setting the `Accept` key to `application/json`.

3. Parse the Response

Once the response is received, you can parse the JSON body of the response by using the `encoding/json` package. This package provides the `json.Unmarshal` function, which takes a byte slice of JSON data and unmarshals it into a Go data structure.

4. Handle Errors

When making an HTTP request, it is important to handle any errors that may be encountered. The `net/http` package provides the `http.Response` type, which contains an `Error` field that can be checked for any errors encountered while making the request. Additionally, the `json.Unmarshal` function can return an error if there is an issue with parsing the JSON data.

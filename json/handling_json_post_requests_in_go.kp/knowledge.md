---
title: Processing JSON post requests with go
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The standard library package `encoding/json` can be used to decode and encode JSON data in Go.
---

**Contents**

[TOC]

## Section 1: Parsing the Request

Go provides a built-in `encoding/json` package for encoding and decoding data in JSON format. To handle a JSON post request, the `json.Unmarshal()` function can be used to parse the request body and store the result in an object.

For example, if the request body is a JSON object with two fields, `name` and `age`, a struct can be created to store the values:

```go
type Person struct {
    Name string
    Age int
}
```

The `json.Unmarshal()` function can then be used to parse the request body and store the result in a `Person` object:

```go
var p Person
err := json.Unmarshal(request.Body, &p)
if err != nil {
    // handle error
}
```

## Section 2: Accessing the Data

Once the request body has been parsed, the data can be accessed from the `Person` object. For example, to access the `name` field:

```go
name := p.Name
```

## Section 3: Error Handling

It is important to handle any errors that may occur while parsing the request body. The `json.Unmarshal()` function returns an `error` object if an error occurs. This should be checked before accessing the data:

```go
err := json.Unmarshal(request.Body, &p)
if err != nil {
    // handle error
}
```

## Section 4: Sending a Response

Once the request has been parsed and the data has been accessed, a response can be sent. The `json.Marshal()` function can be used to convert the data into a JSON object, which can then be sent as the response body:

```go
responseBody, err := json.Marshal(p)
if err != nil {
    // handle error
}

// send response body
```

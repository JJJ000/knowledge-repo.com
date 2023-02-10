---
title: What is the syntax for sending a post request with a body in swift?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: To send a POST request with a body in Swift in JSON, use the `request` method in the URLSession class, passing in the request body as a Data type.
---

**Contents**

[TOC]

## Step 1: Create the URL

Create a URL object with the URL of the endpoint you want to send your POST request to.

```swift
let url = URL(string: "https://example.com/api/endpoint")
```

## Step 2: Create the Request

Create a URLRequest object with the URL you just created and set the method to `.post`.

```swift
var request = URLRequest(url: url)
request.httpMethod = "POST"
```

## Step 3: Set the Request Body

Create a JSON object with the body of the request and set it in the request body.

```swift
let body: [String: Any] = [
    "name": "John Doe",
    "age": 25
]
let jsonData = try? JSONSerialization.data(withJSONObject: body)
request.httpBody = jsonData
```

## Step 4: Send the Request

Create a URLSession object and use the `dataTask` method to send the request and get a response.

```swift
let session = URLSession.shared
let task = session.dataTask(with: request) { data, response, error in
    if let data = data {
        // Handle response
    }
}
task.resume()
```

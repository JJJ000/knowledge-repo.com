---
title: Sending a JSON request with a customized http header field
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: You can use the `X-HTTP-Method-Override` header field to make a POST request with a custom HTTPHeader field in JSON.
---

**Contents**

[TOC]

#### Section 1: Definition of JSON Post

JSON Post is an HTTP request method used to send data to a server. It is analogous to submitting a form, but instead of encoding the data in URL-encoded format, the data is encoded in JSON format.

#### Section 2: Customized HTTPHeader Field

An HTTPHeader field is a line of text that is sent along with an HTTP request or response. It contains information about the request or response, such as the type of content being sent, the length of the content, the language of the content, and more. Customized HTTPHeader fields allow developers to add additional information to the request or response, such as authentication tokens or other data.

#### Section 3: JSON Post with Customized HTTPHeader Field

When making a JSON Post request, developers can include customized HTTPHeader fields in the request. This allows them to add additional information to the request, such as authentication tokens or other data. The server can then use this additional information to process the request appropriately.

#### Section 4: Example of JSON Post with Customized HTTPHeader Field

Below is an example of a JSON Post request with a customized HTTPHeader field. This example includes an authentication token in the HTTPHeader field, which the server can use to authenticate the request.

```
POST /api/users HTTP/1.1
Host: example.com
Content-Type: application/json
Authorization: Bearer <authentication_token>

{
  "name": "John Doe",
  "email": "john@example.com"
}
```

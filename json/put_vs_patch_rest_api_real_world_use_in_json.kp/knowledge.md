---
title: What are the differences between the `PUT` and `PATCH` methods in REST API applications?
authors:
- cool_wizard
tags:
- rest
- api
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-21 00:00:00
updated_at: 2023-01-21 00:00:00
tldr: PUT is used to update an entire resource, while PATCH is used to update only certain parts of a resource.
---

**Contents**

[TOC]

### Use of PUT Method
The PUT method is used when a client wants to replace an existing resource with a new one. This is typically used when a client wants to update an existing resource. The client must provide the entire resource in the request body, and the server will replace the existing resource with the new one.

For example, a client might use the PUT method to update the details of a customer record. The client would send the entire customer record in the request body, and the server would replace the existing record with the new one.

### Use of PATCH Method
The PATCH method is used when a client wants to update only a few fields of an existing resource. This is typically used when a client wants to make a small change to an existing resource. The client can specify which fields should be updated in the request body, and the server will update only those fields.

For example, a client might use the PATCH method to update the address of a customer record. The client would send only the address field in the request body, and the server would update only the address field in the existing record.

### Advantages of Using PUT vs PATCH
Using the PUT method has the advantage of ensuring that the resource is always up-to-date. Since the client must send the entire resource in the request body, the server can be sure that the resource is always in a consistent state.

Using the PATCH method has the advantage of reducing the amount of data that needs to be sent in the request. Since the client can specify which fields should be updated, the server does not need to receive the entire resource in the request body. This can reduce the amount of data sent in the request and improve the performance of the API.

### Disadvantages of Using PUT vs PATCH
Using the PUT method has the disadvantage of requiring the client to always send the entire resource in the request body. This can be inefficient if the client only needs to make a small change to an existing resource.

Using the PATCH method has the disadvantage of not ensuring that the resource is always up-to-date. Since the client can specify which fields should be updated, the server cannot be sure that the resource is always in a consistent state.

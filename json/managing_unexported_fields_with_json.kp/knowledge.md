---
title: Working with JSON data and handling fields that are not exported
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: It is possible to access unexported fields in JSON by using the `omitempty` option in the encoding/json package.
---

**Contents**

[TOC]

## What is JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to exchange data between different applications. It is based on a subset of the JavaScript programming language and is commonly used for client-server communication. JSON is a text-based format that is designed to be human-readable and easily parsed by machines.

## Unexported Fields in JSON

Unexported fields in JSON are fields that are not exported to the client. These fields are usually used for internal purposes and are not intended to be visible to the client. Unexported fields can be used to store sensitive data, such as passwords, that should not be exposed to the public. Unexported fields can also be used to store data that is not needed by the client, such as internal IDs or status codes.

## How to Deal with Unexported Fields

Unexported fields can be dealt with in a number of ways. The most common approach is to use a server-side language to filter out the unexported fields from the JSON response. This can be done by using a library such as JSONPath or by manually iterating through the JSON object and removing the unwanted fields.

Another approach is to use a library such as JSON Schema to define the structure of the JSON object and specify which fields should be exported and which should be unexported. This approach can be used to ensure that only the fields that are intended to be visible to the client are included in the response.

Finally, it is also possible to use encryption or other security measures to protect the data in the unexported fields. This can be done by encrypting the data before it is sent to the client, or by using a secure protocol such as TLS to protect the data in transit.

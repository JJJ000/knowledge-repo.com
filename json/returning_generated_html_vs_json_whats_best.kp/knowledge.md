---
title: Why is it not recommended to return html instead of json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Returning generated HTML instead of JSON is a bad practice because it is not a standard data format and is difficult to parse and manipulate.
---

**Contents**

[TOC]

## Improper Use of HTTP
Returning HTML as a response to an API request violates the HTTP protocol. The response should be in a format that is agreed upon between the client and the server. HTML is not a suitable data format for this purpose.

## Poor Reusability
HTML is not designed to be reused. It is designed to be rendered by a browser. If the data that is being returned is intended to be used in an application, then it should be returned in a format that is designed for reuse, such as JSON.

## Lack of Standardization
HTML is not a standardized format, so it is difficult to ensure that the HTML that is returned is valid and can be parsed properly by the client. JSON, on the other hand, is a standardized format, so it is much easier to ensure that the data can be parsed correctly.

## Security Risks
Returning HTML as a response to an API request can introduce security risks. For example, if the HTML contains JavaScript code, then it could be executed by the client. This could potentially lead to malicious code being executed on the client's machine.

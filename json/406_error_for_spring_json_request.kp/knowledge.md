---
title: A spring JSON request is returning a 406 (not acceptable) status code
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The request is not using an `Accept` header that includes `application/json`.
---

**Contents**

[TOC]

## Introduction
When sending a JSON request to a server, the server may respond with a 406 (not Acceptable) status code. This means that the server does not understand the request and is unable to process it. This can be caused by several different factors, such as incorrect formatting of the JSON request, incorrect content-type header, or incorrect data types in the request body.

## Incorrect Formatting
One of the most common causes of a 406 status code is incorrect formatting of the JSON request. All JSON requests must be properly formatted in order to be understood by the server. This includes ensuring that all key-value pairs are properly separated by commas and that all strings are properly enclosed in quotation marks. If the request is not properly formatted, the server will not be able to understand it and will return a 406 status code.

## Incorrect Content-Type Header
Another common cause of a 406 status code is an incorrect content-type header. All JSON requests must specify a content-type header of "application/json". If the content-type header is not specified or is incorrect, the server will not be able to understand the request and will return a 406 status code.

## Incorrect Data Types
Finally, incorrect data types in the request body can also cause a 406 status code. All data types in the request body must be valid JSON data types such as strings, numbers, booleans, or arrays. If any of the data types are invalid, the server will not be able to understand the request and will return a 406 status code.

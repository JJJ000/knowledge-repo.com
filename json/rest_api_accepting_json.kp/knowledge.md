---
title: Include the "accept application/json" http header when using a rest api
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: Yes, the `Accept application/json` HTTP Header should be used when making requests to a REST API in order to indicate that the response should be in JSON format.
---

**Contents**

[TOC]

## What is the "Accept: application/json" HTTP Header?
The "Accept: application/json" HTTP header is a request header used to indicate that the client is expecting a response in the JSON format. This header is usually sent along with a request to indicate that the server should send its response in the JSON format.

## What is the Purpose of the "Accept: application/json" Header?
The purpose of the "Accept: application/json" header is to ensure that the server sends a response in the JSON format. This is especially important when a client is making a request to a REST API, as the API may not be able to handle requests in other formats.

## How is the "Accept: application/json" Header Used?
The "Accept: application/json" header is typically sent along with a request to indicate that the client is expecting a response in the JSON format. This allows the server to know how to properly format its response.

## What Are the Benefits of Using the "Accept: application/json" Header?
Using the "Accept: application/json" header has several benefits. First, it ensures that the server sends a response in the JSON format, which is often the most efficient format for a REST API. Additionally, it helps to ensure that the server does not send back a response in a format that the client cannot understand. Finally, it helps to ensure that the server is able to properly format the response according to the client's expectations.

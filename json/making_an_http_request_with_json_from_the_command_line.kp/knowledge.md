---
title: What is the command-line method for making an http request with a JSON payload?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can use curl to do an HTTP request/call with a JSON payload from the command-line.
---

**Contents**

[TOC]

## Section 1: Prerequisites

Before attempting to do an HTTP-request with a JSON payload from the command-line, you will need to have the following:

- A command-line interface (CLI)
- cURL (or any other command-line HTTP client)
- A valid JSON payload

## Section 2: Construct the cURL command

Once you have the prerequisites, you can start constructing the cURL command. The basic syntax for the command is as follows:

`curl -X <HTTP_METHOD> -d <JSON_PAYLOAD> <URL>`

Replace the `<HTTP_METHOD>`, `<JSON_PAYLOAD>` and `<URL>` with the appropriate values for your request.

## Section 3: Execute the cURL command

Once you have constructed the cURL command, you can execute it from the command-line. The command should return the response from the server.

## Section 4: Troubleshooting

If you encounter any errors when executing the cURL command, you can use the `-v` flag to enable verbose output, which will provide more information about the request and response.

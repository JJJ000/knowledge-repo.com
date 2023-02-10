---
title: Make a get request using curl with a JSON parameter
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: A cURL GET request with a JSON parameter can be sent by adding the `Content-Type application/json` header and passing the JSON data as the body of the request.
---

**Contents**

[TOC]

## Step 1: Formulate the JSON Parameter

The JSON parameter should be formed in the following format:

```json
{
    "parameter1": "value1",
    "parameter2": "value2"
}
```

## Step 2: Formulate the Curl Command

The curl command should be formulated as follows:

```
curl -X GET "https://example.com" -H "Content-Type: application/json" -d '<JSON parameter>'
```

## Step 3: Insert the JSON Parameter

Replace `<JSON parameter>` in the curl command with the JSON parameter formed in Step 1.

## Step 4: Execute the Curl Command

Execute the curl command in the command line. The response should be returned from the server.

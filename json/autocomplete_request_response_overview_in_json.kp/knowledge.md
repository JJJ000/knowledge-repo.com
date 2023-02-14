---
title: What does an autocomplete request and response from a server look like?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: A typical autocomplete request/server response in JSON format consists of a request object containing a query string, and a response object containing an array of suggested matches.
---

**Contents**

[TOC]

**Request:**
```json
{
  "query": "The quick brown fox"
}
```

**Response:**
```json
{
  "matches": [
    "The quick brown fox jumps over the lazy dog",
    "The quick brown fox ran over the lazy dog",
    "The quick brown fox ate the lazy dog"
  ]
}
```

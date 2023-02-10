---
title: What is the distinction between data and JSON parameters when using the Python requests package?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Data parameters are used to send form-encoded data, while JSON parameters are used to send JSON-encoded data.
---

**Contents**

[TOC]

**Data Parameters**
- Definition: Data parameters are used to send a set of key/value pairs as a JSON object to the server.

- Usage: Data parameters are typically used when making a POST or PUT request to the server.

- Format: Data parameters are sent as JSON objects, which can be easily converted to a Python dictionary.

**JSON Parameters**
- Definition: JSON parameters are used to send a set of key/value pairs as a JSON string to the server.

- Usage: JSON parameters are typically used when making a POST or PUT request to the server.

- Format: JSON parameters are sent as a JSON string, which can be easily converted to a Python dictionary.

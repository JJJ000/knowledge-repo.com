---
title: What are the distinctions between the json.load() and json.loads() functions?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: json.load() loads a JSON file from the specified path, while json.loads() loads a JSON string.
---

**Contents**

[TOC]

# json.load()
The json.load() function takes a file-like object, reads the data from that object, and uses that string to create an object. It is used to deserialize a file containing a JSON document to an object.

# json.loads()
The json.loads() function takes a string as an argument and deserializes it to a Python object. It is used to convert a JSON string to a Python object.

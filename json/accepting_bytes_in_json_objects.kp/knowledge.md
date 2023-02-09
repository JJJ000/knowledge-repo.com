---
title: Allow a JSON object to take in bytes or enable urlopen to generate strings
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, JSON objects do not accept bytes and urlopen output strings cannot be in JSON format.
---

**Contents**

[TOC]

# Accepting Bytes

JSON objects can accept bytes as input. Bytes are a type of data type in Python that can be used to represent binary data. This can be used to store binary data such as images, audio, and video. The bytes can be converted to a string using the decode() method, which will allow the JSON object to parse the data.

# Outputting Strings

JSON objects can also output strings when used with the urlopen() function. This function allows the user to open a URL and retrieve data from it. The data can be a JSON object, which can be converted to a string using the json.dumps() method. This method will take the JSON object and convert it to a string, which can then be used by the JSON object.

---
title: Comparing the process of decoding JSON using json.unmarshal and json.newdecoder.decode
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: json.Unmarshal is used to decode a JSON string into a predefined struct, while json.NewDecoder.Decode is used to decode a JSON string into an arbitrary data structure.
---

**Contents**

[TOC]

# json.Unmarshal

json.Unmarshal is a function in the encoding/json package of the Go programming language. It is used to parse a JSON-encoded byte slice into a Go data structure. It takes two parameters, the byte slice and a pointer to the data structure to be filled with the decoded data. It returns an error if the byte slice is not valid JSON.

# json.NewDecoder.Decode

json.NewDecoder.Decode is also a function in the encoding/json package of the Go programming language. It is used to parse a JSON-encoded stream of bytes into a Go data structure. It takes two parameters, a reader object and a pointer to the data structure to be filled with the decoded data. It returns an error if the stream of bytes is not valid JSON.

# Differences

The main difference between json.Unmarshal and json.NewDecoder.Decode is that json.Unmarshal takes a byte slice as its parameter, while json.NewDecoder.Decode takes a reader object. This means that json.Unmarshal can only be used to parse a single JSON object, while json.NewDecoder.Decode can be used to parse a stream of JSON objects.

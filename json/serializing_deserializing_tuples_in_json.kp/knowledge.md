---
title: What is the process of converting a tuple into and out of JSON format?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: A Tuple can be serialized to JSON by converting it to a list, and can be deserialized by converting the JSON back into a tuple.
---

**Contents**

[TOC]

### Serialization

When serializing a Tuple to JSON, each element of the Tuple will be converted to a JSON element. For example, if the Tuple is (1, 2, 3), the resulting JSON will be `[1, 2, 3]`.

### Deserialization

When deserializing a Tuple from JSON, the JSON elements will be converted to the corresponding Tuple elements. For example, if the JSON is `[1, 2, 3]`, the resulting Tuple will be (1, 2, 3).

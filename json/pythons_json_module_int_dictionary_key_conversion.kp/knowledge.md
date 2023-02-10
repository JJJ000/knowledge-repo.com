---
title: The JSON module in Python converts integer dictionary keys into strings
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, Python`s JSON module automatically converts int dictionary keys to strings.
---

**Contents**

[TOC]

1. Overview

Python's json module is a built-in library that allows users to easily serialize and deserialize data in the JSON (JavaScript Object Notation) format. It is commonly used for data exchange between web applications and other systems.

2. Int Dictionary Keys

In a Python dictionary, keys can be any immutable type, including ints. However, when using the json module to serialize a dictionary, int keys will be converted to strings. This is because JSON only supports string keys in its data structures.

3. Serialization

When serializing a dictionary with the json module, int keys will be converted to strings. This means that any int keys will be converted to strings before being added to the JSON data structure.

4. Deserialization

When deserializing a JSON data structure with the json module, any string keys that represent ints will be converted back to ints. This means that any ints that were converted to strings during serialization will be converted back to ints during deserialization.

---
title: How do the JSON and simplejson Python modules differ?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The JSON module is part of the Python standard library, whereas simplejson is an external library.
---

**Contents**

[TOC]

1. **Data Representation** 

JSON: Data is represented as a string.

SimpleJSON: Data is represented as a native Python object.

2. **Encoding** 

JSON: Uses the standard JSON encoding.

SimpleJSON: Uses a custom encoding that allows for faster parsing and serialization.

3. **Parsing** 

JSON: Uses a standard parser.

SimpleJSON: Uses a custom parser that is faster than the standard parser.

4. **Compatibility** 

JSON: Compatible with most programming languages.

SimpleJSON: Compatible with Python only.

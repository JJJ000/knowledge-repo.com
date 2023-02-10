---
title: Is it possible to prevent gson from changing "<" and ">" into unicode escape sequences?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, Gson will always convert `<` and `>` into unicode escape sequences when serializing to JSON.
---

**Contents**

[TOC]

## Section 1: Overview

Gson is a Java library that can be used to convert Java objects into their JSON representation. It provides a powerful API for serializing and deserializing objects. By default, Gson will convert certain characters such as "<" and ">" into unicode escape sequences when converting to JSON.

## Section 2: How to Avoid

Fortunately, Gson provides a way to avoid this conversion. By setting the `HtmlSafe` flag to `false` when creating the Gson instance, Gson will not convert these characters into unicode escape sequences.

## Section 3: Example

Here is an example of how to create a Gson instance with `HtmlSafe` set to `false`:

```java
Gson gson = new GsonBuilder().setHtmlSafe(false).create();
```

## Section 4: Conclusion

In conclusion, Gson can be configured to avoid converting "<" and ">" into unicode escape sequences in JSON. This can be accomplished by setting the `HtmlSafe` flag to `false` when creating the Gson instance.

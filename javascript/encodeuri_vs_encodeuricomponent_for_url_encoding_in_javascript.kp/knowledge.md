---
title: What is the difference between encodeuri and encodeuricomponent when encoding urls?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: It depends on the type of characters you are encoding, but generally encodeURIComponent is the preferred method.
---

**Contents**

[TOC]

# encodeURI

`encodeURI` is used to encode a Uniform Resource Identifier (URI) by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character. This is useful for encoding URLs, as it ensures that the URL remains valid.

# encodeURIComponent

`encodeURIComponent` is used to encode a Uniform Resource Identifier (URI) component by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character. This is useful for encoding parts of a URL, such as a query string, as it ensures that the URL remains valid.

# Differences

The main difference between `encodeURI` and `encodeURIComponent` is that `encodeURI` encodes the entire URL, while `encodeURIComponent` encodes only a part of the URL. `encodeURI` will also encode certain characters that are not encoded by `encodeURIComponent`.

# Use Case

In general, `encodeURI` should be used when encoding an entire URL, while `encodeURIComponent` should be used when encoding a part of a URL. For example, if you are constructing a URL with query parameters, you should use `encodeURIComponent` for each parameter.

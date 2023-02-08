---
title: What is the best way to save PHP arrays json_encode or serialize?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The preferred method to store PHP arrays is to use json\_encode, as it is more human-readable and easier to work with.
---

**Contents**

[TOC]

## json_encode

json_encode is a function in PHP which takes an array and converts it into a JSON string. It is the preferred method for storing arrays because it is faster and easier to read than serialization. JSON is also a widely used data interchange format, so it is easier to share data between different platforms and applications.

## Serialize

Serialize is a function in PHP which takes an array and converts it into a string. It is not as widely used as json_encode, and it is slower and more difficult to read. Serialization is more secure than json_encode, as it prevents malicious code from being executed. It is also more flexible, as it can store more complex data structures.

---
title: What are the dangers of using the highest level of JSON arrays, and why are they a potential security risk?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Top level JSON arrays are arrays that are directly used as the root level of a JSON object, which can be used for malicious injection attacks.
---

**Contents**

[TOC]

#### What are "top level JSON arrays"?
A top level JSON array is an array that is placed at the root of a JSON document. This means that the array is not nested inside an object.

#### Why are they a security risk in JSON?
Top level JSON arrays can lead to security risks in JSON because they can be used to bypass security checks that are designed to prevent malicious code from being executed. For example, if a top level array is used to store user input, it may be possible for an attacker to inject malicious code into the array and execute it without the security checks being triggered. This can lead to serious security vulnerabilities.

Additionally, top level arrays can lead to unexpected behavior when parsing the JSON document. This can cause the application to crash or behave in an unexpected way, which can lead to security issues.

Finally, top level arrays can make it difficult to identify the structure of the JSON document. This can make it difficult to validate the data and can lead to security vulnerabilities.

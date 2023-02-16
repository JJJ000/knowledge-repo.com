---
title: An error has occurred because a dictionary cannot be used as a key for another dictionary
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Dictionaries cannot be used as keys in a dictionary because they are not hashable.
---

**Contents**

[TOC]

## Overview
Using a dict as a key for another dict in JSON is not allowed because dictionaries are not hashable. This means that they cannot be used as a key for another dict in JSON.

## Why Dictionaries Are Not Hashable
Dictionaries are not hashable because they are mutable. This means that their contents can change, which would prevent them from being used as a reliable key for a dict in JSON.

## Alternatives to Using Dictionaries as Keys
Instead of using a dict as a key for another dict in JSON, it is possible to use other data types such as strings, integers, or floats. These data types are hashable and can be used as reliable keys for dicts in JSON.

## Conclusion
Using a dict as a key for another dict in JSON is not allowed because dictionaries are not hashable. To use a reliable key for a dict in JSON, it is necessary to use other data types such as strings, integers, or floats.

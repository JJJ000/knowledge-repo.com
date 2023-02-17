---
title: Jackson JSON marshall ignores getters
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, Jackson will ignore getter methods when converting a Java object to JSON.
---

**Contents**

[TOC]

##### Yes
By default, Jackson JSON marshaller will ignore getter methods when serializing an object. This is because getter methods are not considered to be part of the object's state and are not included in the serialized output.

##### No
Jackson JSON marshaller can be configured to include getter methods when serializing an object. This can be done by enabling the 'SerializationFeature.WRITE_GETTERS_AS_SETTERS' feature in the ObjectMapper. This will cause Jackson to include the getter methods in the serialized output.

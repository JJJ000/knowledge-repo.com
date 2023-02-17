---
title: Serialization with newtonsoft.json produces an empty JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: This could happen if the object being serialized does not contain any public properties or fields.
---

**Contents**

[TOC]

## Possible Causes 

1. The object is empty to begin with. 
2. The object is not configured to serialize properly. 
3. The serializer is not configured correctly. 
4. The object is not being serialized correctly.

## Troubleshooting 

1. Check the object to ensure it is not empty.
2. Ensure the object is properly configured to serialize. 
3. Check the serializer configuration to ensure it is set up correctly. 
4. Verify that the object is being serialized correctly. 

## Resolution 

1. If the object is empty, there is no resolution. 
2. If the object is not configured to serialize properly, configure it to do so.
3. If the serializer is not configured correctly, configure it correctly. 
4. If the object is not being serialized correctly, debug the serialization process.

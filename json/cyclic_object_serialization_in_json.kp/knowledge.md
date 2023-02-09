---
title: Storing an object that has a cyclical object value in a sequence
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: It is not possible to serialize an object that contains cyclic object values in JSON.
---

**Contents**

[TOC]

## Solution

### 1. Serializing the Object
Serializing an object that contains a cyclic object value in JSON can be done by using a library such as JSON.stringify(). This library will convert a JavaScript object into a string that can be used to store the data.

### 2. Handling Circular References
To handle circular references, the library must be configured to detect and replace circular references with a placeholder value. This placeholder value can be a special character, such as an asterisk (*) or a null value.

### 3. Replacing Placeholders
Once the placeholder values have been set, the library can then be used to replace the placeholder values with the actual values when the object is deserialized. This ensures that the original data is preserved while still allowing the object to be serialized.

### 4. Deserializing the Object
Finally, the object can be deserialized by using the same library that was used to serialize it. This will convert the string back into a JavaScript object and the circular references will be restored.

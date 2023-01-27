---
title: What is the process for generating a guid / uuid?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can create a GUID/UUID in Javascript by using the function Math.random().
---

**Contents**

[TOC]

### Generate a GUID

The following code generates a version 4 GUID (a randomly generated UUID):

```javascript
function generateGUID() {
  return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
    var r = Math.random() * 16 | 0, v = c == 'x' ? r : (r & 0x3 | 0x8);
    return v.toString(16);
  });
}
```

### Validate a GUID

The following code validates a GUID (a UUID):

```javascript
function isValidGUID(guid) {
  return /^[0-9a-f]{8}-[0-9a-f]{4}-[1-5][0-9a-f]{3}-[89ab][0-9a-f]{3}-[0-9a-f]{12}$/i.test(guid);
}
```

### Usage

To generate and validate a GUID, use the following code:

```javascript
var guid = generateGUID();
if (isValidGUID(guid)) {
  console.log('Generated GUID is valid: ' + guid);
}
```

### Example Output

The following is an example output when running the code above:

```
Generated GUID is valid: d2e07c44-b1d6-4a7d-8c62-e7e9a6b3f3b3
```

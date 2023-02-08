---
title: Can an error be converted to a string using json.stringify?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, it is not possible to stringify an Error using JSON.stringify.
---

**Contents**

[TOC]

**No, It Is Not Possible**

**Reason 1: Error Objects Are Not Plain Objects**

Error objects are not plain JavaScript objects, and they contain cyclical references, which cannot be stringified. The JSON.stringify() method only works with plain JavaScript objects.

**Reason 2: Error Objects Have Non-Enumerable Properties**

Error objects have non-enumerable properties, which means they cannot be stringified by the JSON.stringify() method.

**Reason 3: Error Objects Have Non-Serializable Properties**

Error objects have non-serializable properties, which means they cannot be serialized by the JSON.stringify() method.

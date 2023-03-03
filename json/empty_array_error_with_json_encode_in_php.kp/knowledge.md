---
title: The PHP json_encode function does not output braces {} when the array being encoded is empty
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: No, PHP`s json\_encode function does not return braces when an array is empty.
---

**Contents**

[TOC]

### Answer

Yes, `json_encode` will not return braces `{}` when the array is empty.

#### Reason

The reason for this is that an empty array is a valid JSON value, and therefore does not need to be surrounded by braces. According to the JSON specification, an array is defined as a sequence of values, and an empty array is simply an empty sequence.

#### Example

For example, `json_encode([])` will return `[]` instead of `{}`.

#### Alternatives

If you would like the output to be `{}` when the array is empty, you can use a ternary operator to check for an empty array and return `{}` if it is empty. For example:

```php
echo json_encode(empty($array) ? {} : $array);
```

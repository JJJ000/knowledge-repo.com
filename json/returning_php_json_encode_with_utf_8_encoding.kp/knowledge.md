---
title: Is there a way to encode PHP "json_encode" with utf-8 instead of unicode?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Set the `JSON\_UNESCAPED\_UNICODE` flag to `false` when calling `json\_encode`.
---

**Contents**

[TOC]

# Section 1: Setting the Character Encoding

When using `json_encode`, you can set the character encoding by passing in the `JSON_UNESCAPED_UNICODE` flag as the second argument. This will tell `json_encode` to use UTF-8 instead of Unicode when encoding the data.

# Section 2: Example Code

Here is an example of how to use the `JSON_UNESCAPED_UNICODE` flag when using `json_encode`:

```
$data = array('foo' => 'bar');
$encodedData = json_encode($data, JSON_UNESCAPED_UNICODE);
```

# Section 3: Output

The output of the above code will be a string encoded in UTF-8, rather than Unicode:

```
"{"foo":"bar"}"
```

# Section 4: Further Reading

For more information on `json_encode` and the `JSON_UNESCAPED_UNICODE` flag, please see the [PHP documentation](https://www.php.net/manual/en/function.json-encode.php).

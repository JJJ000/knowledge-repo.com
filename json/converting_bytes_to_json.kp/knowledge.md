---
title: Transform a bytes array into a JSON structure
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `json.loads()` function to convert a bytes array into JSON format.
---

**Contents**

[TOC]

# Section 1: Convert Bytes to String

The first step to convert a bytes array into JSON format is to convert the bytes array into a string. This can be done using the `.decode()` method.

```
bytes_string = bytes_array.decode()
```

# Section 2: Parse String into JSON

The next step is to parse the string into a JSON object. This can be done using the `json.loads()` method.

```
json_object = json.loads(bytes_string)
```

# Section 3: Access JSON Object

Once the JSON object has been parsed, the data can then be accessed by using the appropriate keys.

```
data = json_object['key']
```

# Section 4: Convert JSON Object to String

Finally, the JSON object can be converted back to a string using the `json.dumps()` method.

```
json_string = json.dumps(json_object)
```

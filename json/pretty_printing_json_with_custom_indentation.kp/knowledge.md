---
title: What is the process for adding personalized indentation when using the JSON module for formatting output?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the indent argument in the json.dumps() function to specify the desired indentation level.
---

**Contents**

[TOC]

# Section 1: Setting Up

The first step in implementing custom indentation when pretty-printing with the JSON module is to import the JSON module. This can be done by using the following code:

```python
import json
```

# Section 2: Configuring JSON

The next step is to configure the JSON module to use the custom indentation. This can be done by using the `indent` parameter, which takes an integer value to indicate the number of spaces to use for indentation. For example, the following code will set the indentation to 4 spaces:

```python
json.dumps(data, indent=4)
```

# Section 3: Pretty-Printing

Once the JSON module is configured, you can use the `dumps()` method to pretty-print the data in the desired format. This method takes a data object as the first argument and an optional `indent` parameter to set the indentation. For example, the following code will pretty-print the data with 4 spaces of indentation:

```python
print(json.dumps(data, indent=4))
```

# Section 4: Output

Finally, the pretty-printed data will be outputted in the desired format. For example, the following code will output the data with 4 spaces of indentation:

```
{
    "name": "John Doe",
    "age": 25
}
```

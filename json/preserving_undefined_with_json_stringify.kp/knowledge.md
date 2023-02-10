---
title: Ensuring that json.stringify does not remove any undefined values
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON.stringify can be passed a replacer function to modify the behavior of the serialization, allowing undefined values to be preserved.
---

**Contents**

[TOC]

### Using Stringify

JSON.stringify will remove undefined values from the output. To preserve undefined values, you can use a replacer function as the second argument to stringify. The replacer function can be used to modify the output of stringify, including replacing undefined values with a placeholder.

### Using a Placeholder

The replacer function can be used to replace undefined values with a placeholder. This placeholder can be anything, but it should be something that can be distinguished from other values in the output. For example, you could use the string “undefined” as the placeholder.

### Replacing with “null”

Another option is to replace undefined values with “null”. This is a valid JSON value, and it can be distinguished from other values in the output.

### Using a Custom Function

The replacer function can also be used to replace undefined values with a custom function. This function can be used to perform any custom logic that is needed to preserve the undefined values.

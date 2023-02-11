---
title: Retrieve the first (or nth) item from a jq JSON parse
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: To get the first (or n`th) element in a jq JSON parsing, use the `.[n]` syntax.
---

**Contents**

[TOC]

# Section 1: Accessing Elements

The simplest way to access elements in a jq json parsing is to use the `.[index]` syntax. This syntax allows you to specify the index of the element you want to access, starting from 0. For example, `.[0]` will access the first element in the json parsing.

# Section 2: Using the 'first' Function

Another way to get the first element in a jq json parsing is to use the `first` function. This function returns the first element in the json parsing, regardless of its index. For example, `first` applied to the following json parsing:

```
[
  "apple",
  "banana",
  "cherry"
]
```

Will return `"apple"`.

# Section 3: Using the 'nth' Function

If you want to access elements other than the first one, you can use the `nth` function. This function allows you to specify the index of the element you want to access, starting from 0. For example, `nth(2)` applied to the same json parsing as above will return `"cherry"`.

# Section 4: Using the 'slice' Function

Finally, you can use the `slice` function to access a range of elements in a jq json parsing. This function takes two arguments: a start index and an end index. The start index is inclusive, while the end index is exclusive. For example, `slice(0,2)` applied to the same json parsing as above will return `["apple", "banana"]`.

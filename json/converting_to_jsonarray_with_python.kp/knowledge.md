---
title: How can I turn a list of numbers into a JSON array using python?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the json.dumps() function to convert a list of numbers to a JSON array.
---

**Contents**

[TOC]

## Section 1: Importing Libraries

In order to convert a list of numbers to a JSON array, we will need to import the `json` library. This can be done by using the following code:

```python
import json
```

## Section 2: Creating the List

The next step is to create a list of numbers. This list can be created using the following code:

```python
nums = [1, 2, 3, 4, 5]
```

## Section 3: Converting the List to JSON

Now that the list has been created, we can use the `json.dumps()` function to convert the list into a JSON array. This can be done using the following code:

```python
json_array = json.dumps(nums)
```

## Section 4: Outputting the JSON Array

Finally, we can output the JSON array using the `print()` function. This can be done using the following code:

```python
print(json_array)
```

The output of this code will be a JSON array, which will look like this:

```json
[1, 2, 3, 4, 5]
```

---
title: Insert a new item into an existing JSON array using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `. +=` operator to add a new element to an existing JSON array with jq.
---

**Contents**

[TOC]

**Section 1: Install jq**

jq is a lightweight and flexible command-line JSON processor. It can be used for manipulating and navigating JSON data. To install jq, use the following command: 

`sudo apt-get install jq`

**Section 2: Create JSON Array**

Create a JSON array with the following elements:

```
{
  "array": [
    "element1",
    "element2",
    "element3"
  ]
}
```

**Section 3: Add New Element to JSON Array**

Use the following command to add a new element to the JSON array:

`jq '.array += ["element4"]'`

**Section 4: Output Updated JSON Array**

The output of the command will be the updated JSON array:

```
{
  "array": [
    "element1",
    "element2",
    "element3",
    "element4"
  ]
}
```

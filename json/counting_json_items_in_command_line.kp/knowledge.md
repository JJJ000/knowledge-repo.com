---
title: What is the command line method for determining the number of items in a JSON object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the `jq` command to count items in a JSON object from the command line.
---

**Contents**

[TOC]

# Section 1: Using jq

The most straightforward way to count items in a JSON object using the command line is to use the jq command. jq is a command-line JSON processor that allows you to filter, transform, and parse JSON data.

# Section 2: Counting Items

To count the number of items in a JSON object, use the following command:

`jq '.|length' <file.json`

This will return the number of items in the JSON object.

# Section 3: Counting Keys

To count the number of keys in a JSON object, use the following command:

`jq 'keys|length' <file.json`

This will return the number of keys in the JSON object.

# Section 4: Counting Values

To count the number of values in a JSON object, use the following command:

`jq 'values|length' <file.json`

This will return the number of values in the JSON object.

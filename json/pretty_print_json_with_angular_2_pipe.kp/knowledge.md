---
title: A pipe in angular 2 that formats a JSON object into a readable, indented version
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The JsonPipe can be used to transform a JSON object into a pretty-printed JSON string.
---

**Contents**

[TOC]

## Section 1: Overview

The Angular 2 pipe for transforming a JSON object to pretty-printed JSON is called the JsonPipe. This pipe is used to perform a deep transformation of a JSON object into a human-readable format. The pipe uses the JSON.stringify() method to perform the transformation.

## Section 2: Usage

The JsonPipe can be used in any Angular 2 template by wrapping the JSON object within the pipe's syntax, i.e. `{{jsonObject | json}}`. This will output the pretty-printed JSON object in the template.

## Section 3: Options

The JsonPipe has a few optional parameters that can be used to customize the output. The first option is the `spaces` parameter, which is used to specify the number of spaces to be used for indentation. The second option is the `toJSON` parameter, which is used to specify a custom toJSON() method to be used for the transformation.

## Section 4: Example

Here is an example of how to use the JsonPipe to pretty-print a JSON object:

```
<pre>{{ jsonObject | json: 2 }}</pre>
```

This will output the JSON object with two spaces of indentation.

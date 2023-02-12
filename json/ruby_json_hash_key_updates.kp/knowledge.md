---
title: Converting hash keys using ruby's JSON parser
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: No, Ruby JSON does not change Hash keys in JSON.
---

**Contents**

[TOC]

## No

Ruby does not change the keys in a JSON object when it parses it. The keys remain the same as in the original JSON file.

## Why

Ruby parses JSON using the `JSON.parse` method, which takes a string and converts it into a Ruby data structure. This method does not modify the keys in any way; it simply converts them into the appropriate Ruby data structure.

## How

When parsing a JSON object, Ruby will convert the keys into symbols or strings, depending on the type of data structure that is being parsed. For example, if the JSON object contains a hash, the keys will be converted into symbols, while if it contains an array, the keys will be converted into strings.

## Example

For example, if we have the following JSON object:

```
{
  "name": "John Doe",
  "age": 42
}
```

When we parse it with Ruby, the resulting data structure will look like this:

```
{
  :name => "John Doe",
  :age => 42
}
```

As you can see, the keys remain the same, but are converted into symbols.

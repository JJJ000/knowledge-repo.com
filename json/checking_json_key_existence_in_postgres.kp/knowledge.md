---
title: Is there a way to determine if a JSON key exists in postgres?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the jsonb\_exists() function to check if a JSON key exists in Postgres.
---

**Contents**

[TOC]

**Checking if a JSON Key Exists in Postgres:**

**Using the `JSON_EXISTS` Function:**

The `JSON_EXISTS` function can be used to check if a particular key exists in a JSON object. This function takes two arguments: a JSON object and a JSON path. The JSON path is a string that specifies the location of the key within the JSON object. For example, `JSON_EXISTS('{"foo": {"bar": "baz"}}', '$.foo.bar')` will return `true`, since the key `bar` exists in the JSON object.

**Using the `JSON_OBJECT_KEYS` Function:**

The `JSON_OBJECT_KEYS` function can be used to retrieve a list of all the keys in a JSON object. This function takes one argument: a JSON object. The returned list can then be used to check if a particular key exists in the JSON object. For example, `JSON_OBJECT_KEYS('{"foo": {"bar": "baz"}}')` will return `['foo']`, which can be used to check if the `foo` key exists.

**Using the `JSON_TYPE` Function:**

The `JSON_TYPE` function can be used to check the type of a particular key in a JSON object. This function takes two arguments: a JSON object and a JSON path. The JSON path is a string that specifies the location of the key within the JSON object. For example, `JSON_TYPE('{"foo": {"bar": "baz"}}', '$.foo.bar')` will return `string`, indicating that the `bar` key is a string.

**Using the `JSON_CONTAINS` Function:**

The `JSON_CONTAINS` function can be used to check if a particular key exists in a JSON object. This function takes three arguments: a JSON object, a JSON path, and a value. The JSON path is a string that specifies the location of the key within the JSON object, and the value is the value to be checked for. For example, `JSON_CONTAINS('{"foo": {"bar": "baz"}}', '$.foo.bar', 'baz')` will return `true`, since the key `bar` exists in the JSON object and its value is `baz`.

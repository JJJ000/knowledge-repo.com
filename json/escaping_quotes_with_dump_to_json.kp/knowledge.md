---
title: Adding extra quotation marks and the escaping of existing quotation marks are both features of dump to json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, Dump to JSON adds additional double quotes and escapes quotes in JSON for valid syntax.
---

**Contents**

[TOC]

**Yes**

**Adding Double Quotes**

When a JSON string is dumped, it will add double quotes around the keys and values. This is necessary to make sure that the data is properly formatted and can be read by the parser.

**Escaping of Quotes**

When a JSON string is dumped, it will also escape any quotes that are in the string. This is done to make sure that the data is properly formatted and can be read by the parser. Escaping quotes means that any quotes in the string are replaced with a backslash followed by the quote character. This ensures that the quotes are not interpreted as part of the string, but rather as part of the formatting of the JSON string.

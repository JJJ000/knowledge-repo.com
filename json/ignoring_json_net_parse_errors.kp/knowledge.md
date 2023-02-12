---
title: Ignore any mistakes made while processing JSON data using json.net
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: IgnoreErrors can be set to true when deserializing with Json.NET to ignore any errors encountered during parsing.
---

**Contents**

[TOC]

1. Using JsonSerializerSettings
--------------------------------
The JsonSerializerSettings class allows you to configure how JSON.NET parses and generates JSON. You can set the `MissingMemberHandling` property to `Ignore` to have JSON.NET ignore any members it doesn't recognize when parsing JSON.

2. Using JsonTextReader
-----------------------
The JsonTextReader class provides a way to read JSON from a TextReader. You can set the `MaxDepth` property to `null` to have JSON.NET ignore any members it doesn't recognize when parsing JSON.

3. Using JsonReaderException
----------------------------
The JsonReaderException class provides a way to catch errors when parsing JSON. You can set the `ErrorHandling` property to `Ignore` to have JSON.NET ignore any errors it encounters when parsing JSON.

4. Using JsonLoadSettings
-------------------------
The JsonLoadSettings class allows you to configure how JSON.NET parses JSON. You can set the `IgnoreErrors` property to `true` to have JSON.NET ignore any errors it encounters when parsing JSON.

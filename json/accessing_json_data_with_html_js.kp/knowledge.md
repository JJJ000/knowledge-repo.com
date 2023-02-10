---
title: How to access JSON data loaded in a script tag using html and JavaScript with the src attribute set
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The JSON data can be accessed using the `fetch` API.
---

**Contents**

[TOC]

1. Accessing JSON Data with `JSON.parse()`

The `JSON.parse()` method can be used to access JSON data loaded in a script tag with `src` set to a JSON file. This method takes a single argument, a JSON-formatted string, and returns a JavaScript object.

2. Accessing JSON Data with `document.currentScript`

The `document.currentScript` method can be used to access the script tag containing the JSON data. This method returns the `<script>` element whose `src` attribute is set to the JSON file.

3. Accessing JSON Data with `fetch()`

The `fetch()` method can be used to access JSON data loaded in a script tag with `src` set to a JSON file. This method takes a single argument, the URL of the JSON file, and returns a `Promise` object.

4. Accessing JSON Data with `XMLHttpRequest`

The `XMLHttpRequest` object can be used to access JSON data loaded in a script tag with `src` set to a JSON file. This object takes a single argument, the URL of the JSON file, and returns a `XMLHttpRequest` object.

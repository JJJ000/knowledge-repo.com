---
title: What is the process for accessing a JSON file stored on a local device using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `fetch()` API to read an external local JSON file in JavaScript.
---

**Contents**

[TOC]

## Section 1: Create a local JSON file

1. Create a new file with the .json extension.
2. Enter the data you want to store in the JSON file.
3. Save the file in the same directory as your HTML file.

## Section 2: Include the JSON file in HTML

1. Include a `<script>` tag in the HTML file.
2. Set the `src` attribute of the `<script>` tag to the path of the JSON file.

## Section 3: Read the JSON file in JavaScript

1. Use the `fetch()` method to read the JSON file.
2. The `fetch()` method returns a Promise, which resolves to a Response object.
3. Use the `.json()` method of the Response object to get the JSON data.

## Section 4: Use the JSON data

1. The `.json()` method returns a Promise, which resolves to the JSON data.
2. Use the `.then()` method to access the JSON data.
3. Once you have the JSON data, you can use it in your JavaScript code.

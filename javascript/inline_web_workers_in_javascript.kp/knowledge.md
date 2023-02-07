---
title: What are web workers that do not have a separate JavaScript file?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Web workers can be created inline in the same file using the Blob constructor.
---

**Contents**

[TOC]

## Using Inline Scripts 
Web workers can be created using inline scripts, which are scripts that are directly embedded within the HTML code. This is done by creating a new `<script>` tag with the `type` attribute set to `"text/javascript"` and the `src` attribute set to `"data:text/javascript;base64,[base64-encoded-javascript-code]"`. The JavaScript code within the `src` attribute is then Base64 encoded and can be used to create a web worker.

## Using Blob URLs 
Web workers can also be created using blob URLs. This is done by creating a new `Blob` object with the JavaScript code as its content, and then creating a new `URL` object with the `Blob` object as its parameter. This will create a new blob URL which can then be used to create a web worker.

## Using Data URIs 
Web workers can also be created using data URIs. This is done by creating a new `<script>` tag with the `type` attribute set to `"text/javascript"` and the `src` attribute set to `"data:[mimetype],[encoded-data]"`. The JavaScript code within the `src` attribute is then encoded and can be used to create a web worker.

## Using String Literals
Web workers can also be created using string literals. This is done by creating a new `<script>` tag with the `type` attribute set to `"text/javascript"` and the `src` attribute set to `"javascript:[javascript-code]"`. The JavaScript code within the `src` attribute can then be used to create a web worker.

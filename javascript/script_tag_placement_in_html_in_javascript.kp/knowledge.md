---
title: What is the correct location to insert <script> tags in html code?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Script tags should be placed within the <head> or <body> tags of an HTML document.
---

**Contents**

[TOC]

1. `<head>` Section
2. `<body>` Section

## <head> Section

The `<script>` tag should be placed in the `<head>` section of the HTML markup. This is the most common and recommended way of including scripts in an HTML document. The `<script>` tag should be placed before the `</head>` tag. This ensures that the script is loaded and executed before any other content in the document is rendered.

## <body> Section

The `<script>` tag can also be placed in the `<body>` section of the HTML markup. This is not the most common way of including scripts, but it can be useful in certain situations. Placing the `<script>` tag at the bottom of the `<body>` section can help improve the loading performance of the HTML document, as it ensures that the script is not loaded until the rest of the content has been rendered.

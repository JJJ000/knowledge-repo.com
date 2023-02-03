---
title: Insert another html file into a html file
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can include another HTML file in a HTML file using the <script> tag with the `src` attribute set to the path of the HTML file.
---

**Contents**

[TOC]

## Using the HTML <script> Tag

The <script> tag can be used to include an external HTML file in a HTML file. The <script> tag should be used in the <head> section of the HTML file, and the `src` attribute should be used to specify the path of the external HTML file.

```html
<head>
  <script src="path/to/external/file.html"></script>
</head>
```

## Using the HTML <iframe> Tag

The <iframe> tag can also be used to include an external HTML file in a HTML file. The <iframe> tag should be placed where the external HTML file should be displayed in the HTML file. The `src` attribute should be used to specify the path of the external HTML file.

```html
<body>
  <iframe src="path/to/external/file.html"></iframe>
</body>
```

## Using the HTML <object> Tag

The <object> tag can also be used to include an external HTML file in a HTML file. The <object> tag should be placed where the external HTML file should be displayed in the HTML file. The `data` attribute should be used to specify the path of the external HTML file.

```html
<body>
  <object data="path/to/external/file.html"></object>
</body>
```

## Using the HTML <embed> Tag

The <embed> tag can also be used to include an external HTML file in a HTML file. The <embed> tag should be placed where the external HTML file should be displayed in the HTML file. The `src` attribute should be used to specify the path of the external HTML file.

```html
<body>
  <embed src="path/to/external/file.html"></embed>
</body>
```

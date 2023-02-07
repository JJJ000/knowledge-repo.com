---
title: What is the correct format for using ng-include?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The correct syntax of ng-include in Javascript is `ng-include=``path/to/template.html``
---

**Contents**

[TOC]

1. Syntax

`<div ng-include="'path/to/template.html'"></div>`

2. Attributes

| Attribute | Description |
| --------- | ----------- |
| `ng-include` | Required. Specifies the URL of the HTML template to include |

3. Example

```html
<div ng-include="'app/templates/template.html'"></div>
```

4. Notes

- The URL of the template can be an absolute URL or a relative URL.
- The template can be a single file or multiple files.
- The template can be an HTML fragment or a full HTML document.

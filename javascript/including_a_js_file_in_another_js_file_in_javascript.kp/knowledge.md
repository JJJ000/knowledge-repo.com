---
title: What is the proper syntax for including a JavaScript file in another JavaScript file?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can include a JavaScript file in another JavaScript file by using the `<script>` tag with the `src` attribute.
---

**Contents**

[TOC]

### Using the Script Tag

The traditional way of including a JavaScript file in another JavaScript file is to use the `<script>` tag. You can include a JavaScript file inside another JavaScript file using the `<script>` tag, and its `src` attribute.

```html
<script src="path/to/file.js"></script>
```

### Using the import Statement

Another way to include a JavaScript file in another JavaScript file is to use the `import` statement. The `import` statement allows you to import an entire module or individual objects from a module.

```javascript
import { object1, object2 } from 'path/to/file.js';
```

### Using the require Statement

The `require` statement is another way to include a JavaScript file in another JavaScript file. The `require` statement is used to load a module and its dependencies.

```javascript
const module = require('path/to/file.js');
```

---
title: Send a PHP string to a JavaScript variable and make sure to escape any line breaks
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `escape` function to escape the newlines in the string and assign the string to a JavaScript variable using the `var` keyword.
---

**Contents**

[TOC]

### Section 1: Create a PHP Variable

```php
$phpString = "This is a \nPHP string";
```

### Section 2: Output the PHP Variable as a JavaScript Variable

```php
echo "<script>var jsString = '" . str_replace(array("\r\n", "\r", "\n"), '\n', $phpString) . "';</script>";
```

### Section 3: Output the JavaScript Variable

```js
console.log(jsString);
```

### Section 4: Result

The output of the JavaScript variable will be:

```
This is a \nPHP string
```

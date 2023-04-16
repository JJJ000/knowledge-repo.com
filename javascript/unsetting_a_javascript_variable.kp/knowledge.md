---
title: What is the best way to clear a JavaScript variable?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can unset a JavaScript variable by setting it to `null`.
---

**Contents**

[TOC]

### Using the `delete` Operator
The `delete` operator can be used to unset a JavaScript variable. This operator should be used with caution, as it can have unexpected consequences.

Syntax:
```
delete variable_name;
```

Example:
```
var myVariable = 10;
delete myVariable;
```

### Using the `undefined` Value
The `undefined` value can be used to unset a JavaScript variable. This is the recommended approach as it does not have any unexpected consequences.

Syntax:
```
variable_name = undefined;
```

Example:
```
var myVariable = 10;
myVariable = undefined;
```

---
title: Toggle jquery submit button on/off
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: jQuery can enable or disable a submit button by using the .prop() method.
---

**Contents**

[TOC]

#Solution 1

Using jQuery:

```javascript
$("#submitButton").prop("disabled", true); // To disable
$("#submitButton").prop("disabled", false); // To enable
```

#Solution 2

Using plain JavaScript:

```javascript
document.getElementById("submitButton").disabled = true; // To disable
document.getElementById("submitButton").disabled = false; // To enable
```

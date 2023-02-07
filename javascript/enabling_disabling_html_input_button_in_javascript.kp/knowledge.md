---
title: Toggling a html input button on and off
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To disable an input button, set its `disabled` attribute to `true`; to enable it, set the attribute to `false`.
---

**Contents**

[TOC]

#### Disabling

To disable an HTML input button in Javascript, you can set the `disabled` attribute to `true`:

```javascript
document.getElementById("myButton").disabled = true;
```

#### Enabling

To enable an HTML input button in Javascript, you can set the `disabled` attribute to `false`:

```javascript
document.getElementById("myButton").disabled = false;
```

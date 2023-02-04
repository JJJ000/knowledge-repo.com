---
title: Open the url in the same browser window and tab
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: window.location.href=`url` can be used to open a URL in the same window and tab.
---

**Contents**

[TOC]

# Option 1

Using `window.location`:

```javascript
window.location = 'http://www.example.com';
```

# Option 2

Using `window.location.replace`:

```javascript
window.location.replace('http://www.example.com');
```

# Option 3

Using `window.location.assign`:

```javascript
window.location.assign('http://www.example.com');
```

# Option 4

Using `window.open`:

```javascript
window.open('http://www.example.com', '_self');
```

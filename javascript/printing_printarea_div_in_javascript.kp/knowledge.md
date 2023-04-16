---
title: Only display the content of the <div id="printarea"></div> element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: document.getElementById(`printarea`).innerHTML;
---

**Contents**

[TOC]

**1. Create Element**

```javascript
let printDiv = document.createElement('div');
printDiv.id = 'printarea';
```

**2. Append Element**

```javascript
document.body.appendChild(printDiv);
```

**3. Add Content**

```javascript
printDiv.innerHTML = '<p>This is the content of the div.</p>';
```

**4. Print Element**

```javascript
window.print(printDiv);
```

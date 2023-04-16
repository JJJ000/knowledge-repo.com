---
title: A bootstrap modal appearing behind the background
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `z-index` CSS property to ensure the modal is on top of the background.
---

**Contents**

[TOC]

#Solution 1:

Using z-index:

1. Set the z-index of your modal to a value greater than that of the background.

2. Add the following CSS to your modal:

```
.modal {
    position: absolute;
    z-index: 999;
}
```

#Solution 2:

Using opacity:

1. Set the opacity of the background to a value lower than that of the modal.

2. Add the following CSS to your background:

```
.background {
    opacity: 0.5;
}
```

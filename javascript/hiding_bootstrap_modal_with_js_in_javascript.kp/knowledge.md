---
title: What is the JavaScript code to close a bootstrap modal?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the jQuery hide() method to hide a Bootstrap modal with JavaScript.
---

**Contents**

[TOC]

### Section 1: Select the Modal Element

The first step to hiding a Bootstrap modal with JavaScript is to select the modal element. This can be done using the `document.querySelector()` method.

### Section 2: Hide the Modal

Once the modal element is selected, the modal can be hidden using the `modal.style.display = "none";` command. This will hide the modal from view.

### Section 3: Show the Modal

If the modal needs to be shown again, the `modal.style.display = "block";` command can be used to show the modal again.

### Section 4: Toggle the Modal

To toggle the modal between being hidden and visible, the `modal.style.display = modal.style.display === "none" ? "block" : "none";` command can be used. This will toggle the modal between being hidden and visible.

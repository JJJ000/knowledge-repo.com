---
title: Prevent closing of bootstrap modal when clicking outside of its boundaries
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The modal can be closed by setting the backdrop option to `static` when initializing the modal.
---

**Contents**

[TOC]

### Section 1: Prevent Modal Closing

To prevent the modal from closing when a user clicks outside of the modal area, you can use the `backdrop: 'static'` option when initializing the modal. This will prevent the modal from closing when a user clicks outside of the modal area.

### Section 2: Add Event Listener

You can also add an event listener to the modal's backdrop element to prevent the modal from closing when a user clicks outside of the modal area.

### Section 3: Prevent Default Action

You can also prevent the default action of closing the modal when a user clicks outside of the modal area by using the `event.preventDefault()` method.

### Section 4: Stop Propagation

Finally, you can also stop the click event from propagating to the modal's backdrop element by using the `event.stopPropagation()` method. This will prevent the modal from closing when a user clicks outside of the modal area.

---
title: Is it possible to create a <button> that does not submit a form?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can prevent a <button> from submitting a form by using the `event.preventDefault()` method in the button`s click event listener.
---

**Contents**

[TOC]

**Yes, You Can Make a Button Not Submit a Form in Javascript**

**Section 1: Using the onclick Event**

You can use the onclick event to prevent a form from being submitted. This is done by adding an onclick event to the button element, and then using the preventDefault() method. This will stop the form from being submitted.

**Section 2: Using the return False Statement**

Another way to prevent a form from being submitted is to use the return false statement. This can be added to the onclick event of the button element. The return false statement will prevent the form from being submitted when the button is clicked.

**Section 3: Using the preventDefault() Method**

The preventDefault() method can also be used to prevent a form from being submitted. This method can be added to the onclick event of the button element. This will stop the form from being submitted when the button is clicked.

**Section 4: Using the stopPropagation() Method**

The stopPropagation() method can also be used to prevent a form from being submitted. This method can be added to the onclick event of the button element. This will stop the form from being submitted when the button is clicked.

---
title: How can I use jquery to get values from form input fields?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: jQuery can be used to obtain form input fields using the $(`input`) selector.
---

**Contents**

[TOC]

**Section 1: Selecting Form Inputs**

Using jQuery, you can select form input fields by using the `$('input')` selector. This will select all input fields on the page, including text fields, checkboxes, radio buttons, and more.

**Section 2: Selecting Specific Input Types**

If you want to select only specific types of inputs, you can use the `$('input[type=<type>]')` selector. For example, `$('input[type=text]')` will select only text fields.

**Section 3: Selecting Specific Inputs**

If you want to select a specific input field, you can use the `$('#<id>')` selector. This will select the input field with the specified ID.

**Section 4: Selecting Multiple Inputs**

To select multiple inputs, you can use the `$('input, select, textarea')` selector. This will select all input, select, and textarea fields on the page.

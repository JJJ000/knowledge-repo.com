---
title: Using jquery to check a checkbox
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: $(`input[type=`checkbox`]`).prop(`checked`, true);
---

**Contents**

[TOC]

1. Select the Checkbox 
    To select a checkbox using jQuery, use the attr() method to set the attribute "checked" to true.

2. Syntax 
    The syntax for this is:
    ```javascript
    $(selector).attr('checked', true);
    ```

3. Example
    For example, the following code will select the checkbox with the id "checkbox1":
    ```javascript
    $('#checkbox1').attr('checked', true);
    ```

4. Considerations 
    Note that this does not trigger any events associated with the checkbox. If you need to trigger events, use the .prop() method instead.

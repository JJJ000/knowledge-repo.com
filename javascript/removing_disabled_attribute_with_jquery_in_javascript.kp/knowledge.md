---
title: What is the best way to use jquery to remove the "disabled" attribute?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `disabled` attribute can be removed using jQuery by calling the removeAttr() method.
---

**Contents**

[TOC]

1. Select the Element 

Using jQuery, you can select the element that has the `disabled` attribute. You can do this by using the `$()` function and passing in the `[disabled]` selector.

2. Remove the Attribute

Once the element has been selected, you can remove the `disabled` attribute by using the `removeAttr()` method. This will remove the attribute from the selected element.

3. Set the Attribute to False

Alternatively, you can also set the `disabled` attribute to `false` instead of removing it. This can be done by using the `attr()` method and passing in `disabled` as the attribute and `false` as the value.

4. Confirm the Change

Finally, you can confirm that the `disabled` attribute has been removed or set to `false` by using the `hasAttr()` method. This will return a boolean value indicating if the attribute is present or not.

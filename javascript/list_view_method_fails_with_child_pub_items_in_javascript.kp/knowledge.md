---
title: The 'getlistitemxmlattributes' method of the list view fails when dealing with child publication items
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The getListItemXmlAttributes method does not work with child publication items in Javascript.
---

**Contents**

[TOC]

**Section 1: Overview of the Problem**

When attempting to use the getListItemXmlAttributes method on a child publication item in a List view, the method fails with a Javascript error. This issue occurs when attempting to access the data of an item that is not part of the current List view.

**Section 2: Causes of the Problem**

The issue is caused by the fact that the getListItemXmlAttributes method is intended to be used on items that are part of the current List view. When attempting to access the data of an item that is not part of the current List view, the method fails.

**Section 3: Workarounds**

A workaround for this issue is to use the getItemById method to retrieve the item from the List view, then use the getListItemXmlAttributes method on the retrieved item. This will ensure that the method is only being used on items that are part of the current List view.

**Section 4: Conclusion**

In conclusion, when attempting to use the getListItemXmlAttributes method on a child publication item in a List view, the method fails with a Javascript error. This issue can be resolved by using the getItemById method to retrieve the item from the List view, then using the getListItemXmlAttributes method on the retrieved item.

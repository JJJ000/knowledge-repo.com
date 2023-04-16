---
title: What is the process for adding text to a div element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To append text to a div element in Javascript, use the innerHTML property to add the desired text.
---

**Contents**

[TOC]

1. Select the Element

First, you need to select the element you want to append text to. You can do this by using the `getElementById()` method. This method takes in a string argument that is the id of the element you want to select.

2. Create Text Node

Once you have selected the element, you need to create a text node. You can do this by using the `createTextNode()` method. This method takes in a string argument that is the text you want to append to the element.

3. Append Text

Now you can append the text to the element. You can do this by using the `appendChild()` method. This method takes in a node argument that is the text node you created in the previous step.

4. Update the DOM

Finally, you need to update the DOM to reflect the changes you made. You can do this by using the `updateDOM()` method. This method takes in no arguments and updates the DOM with the changes you made.

---
title: Positioning a div in the center of the screen using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: $(`#divID`).css(`margin`,`auto`);
---

**Contents**

[TOC]

## Step 1: Select the DIV 

Using jQuery, you can select the DIV you want to center on the screen with the `$('#divID')` selector. 

## Step 2: Calculate the Position

To center the DIV, you need to calculate its position. To do this, you can use the `$(window).width()` and `$(window).height()` methods to get the width and height of the window, respectively. Then, you can subtract the width and height of the DIV from the window width and height to get the top and left positions of the DIV. 

## Step 3: Set the Position

Once you have the position of the DIV, you can set it using the `.css()` method. For example, you can use `$('#divID').css('top', topPosition + 'px')` and `$('#divID').css('left', leftPosition + 'px')` to set the top and left positions of the DIV. 

## Step 4: Center the DIV

Finally, you can use the `.css()` method to center the DIV. You can use `$('#divID').css('margin', 'auto')` to center the DIV horizontally and `$('#divID').css('position', 'absolute')` to center the DIV vertically.

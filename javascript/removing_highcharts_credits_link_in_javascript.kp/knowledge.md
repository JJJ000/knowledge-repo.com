---
title: Taking away the highcharts.com attribution link
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The credits link can be removed by setting the credits.enabled option to false in the chart options.
---

**Contents**

[TOC]

## Solution 1

The easiest way to remove the credits link from a Highcharts chart is to set the `credits.enabled` option to `false` in the chart's configuration object. This will prevent the link from being displayed.

## Solution 2

Alternatively, you can also use the `credits.text` option to specify custom text for the credits link. This will replace the default link with the specified text.

## Solution 3

You can also use the `credits.href` option to remove the link altogether. Setting this option to `null` will prevent the link from being displayed.

## Solution 4

Finally, you can use the `credits.position` option to move the credits link to an arbitrary position on the chart. This will allow you to position the link in a way that is less intrusive.

---
title: What is the best way to identify a mobile device using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use jQuery`s `navigator.userAgent` property to detect a mobile device.
---

**Contents**

[TOC]

## Step 1: Include jQuery

Include a reference to the jQuery library in your HTML document.

```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
```

## Step 2: Use window.navigator

Use the window.navigator object in JavaScript to detect a mobile device.

```
if( /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent) ) {
   // some code..
}
```

## Step 3: Use jQuery

Use jQuery's .width() method to detect the width of the device.

```
if ($(window).width() < 768) {
   // some code..
}
```

## Step 4: Use jQuery Mobile

Use jQuery Mobile's .support.orientation method to detect if the device supports orientation.

```
if ($.mobile.support.orientation) {
   // some code..
}
```

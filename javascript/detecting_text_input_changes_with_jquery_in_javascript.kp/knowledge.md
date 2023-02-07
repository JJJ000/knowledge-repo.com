---
title: Use jquery to immediately detect any alterations to an <input type="text"> element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: $(`input[type=`text`]`).on(`change`, function(){ //Do something });
---

**Contents**

[TOC]

1. Event Handler:
```javascript
$("input[type='text']").on('change', function(){
    //code to handle change
});
```
2. Event Listener:
```javascript
$("input[type='text']").addEventListener('change', function(){
    //code to handle change
});
```
3. Keyup Event:
```javascript
$("input[type='text']").keyup(function(){
    //code to handle change
});
```
4. Keydown Event:
```javascript
$("input[type='text']").keydown(function(){
    //code to handle change
});
```

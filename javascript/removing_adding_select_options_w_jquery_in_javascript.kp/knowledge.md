---
title: What is the process for clearing all the options of a select box in jquery, then adding one option and selecting it?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the `.empty()` method to remove all options, then use the `.append()` method to add the desired option and `.val()` to select it.
---

**Contents**

[TOC]

### Removing Options

Using the jQuery `remove()` method, all options in the select box can be removed:

```javascript
$('#selectBox option').remove();
```

### Adding Option

To add a single option to the select box, use the jQuery `append()` method:

```javascript
$('#selectBox').append($('<option>', { 
    value: 'optionValue',
    text : 'optionText'
}));
```

### Selecting Option

To select the option that was just added, use the jQuery `val()` method:

```javascript
$('#selectBox').val('optionValue');
```

### Combining Steps

The steps above can be combined into a single statement:

```javascript
$('#selectBox').empty().append($('<option>', { 
    value: 'optionValue',
    text : 'optionText'
})).val('optionValue');
```

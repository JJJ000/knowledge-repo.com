---
title: Display jquery ui datepicker with month and year only
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `changeMonth` and `changeYear` options to enable the user to select a month and year only with the jQuery UI DatePicker.
---

**Contents**

[TOC]

### Step 1: Include jQuery UI

Include the jQuery UI library in your HTML file.

```html
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
```

### Step 2: Initialize DatePicker

Initialize the DatePicker in your JavaScript file.

```javascript
$(function() {
  $("#datepicker").datepicker();
});
```

### Step 3: Set Date Format

Set the date format to show month and year only.

```javascript
$(function() {
  $("#datepicker").datepicker({
    dateFormat: 'mm/yy'
  });
});
```

### Step 4: Add Input Field

Add an input field to your HTML file.

```html
<input type="text" id="datepicker">
```

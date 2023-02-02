---
title: Retrieve the chosen text from a drop-down menu (select box) using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: jQuery can be used to get the selected text from a drop-down list (select box) using the .find(`optionselected`) selector.
---

**Contents**

[TOC]

#1. HTML Setup

In order to use jQuery to select text from a drop-down list, you must first set up the HTML for the select box. The HTML should look like this:

```
<select id="dropdown">
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</select>
```

#2. jQuery Syntax

Once the HTML is set up, you can use jQuery to select the text from the drop-down list. The syntax for this is as follows:

```
var selectedText = $("#dropdown option:selected").text();
```

#3. Output

The selected text from the drop-down list will be stored in the variable `selectedText`. This can then be used to output the text in the following way:

```
console.log(selectedText);
```

#4. Example

For example, if the user selected `Option 2` from the drop-down list, the output would be:

```
Option 2
```

---
title: Retrieve the text of a specific <option> element using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the jQuery .text() method to get the text of a specific option tag.
---

**Contents**

[TOC]

### Section 1: Selecting the Option Tag

To select an option tag with jQuery, you can use the `$()` function. This function takes a selector as an argument, and you can use the `option` tag selector to select any option tag on the page.

For example, to select an option tag with the value of "foo", you could use the following code:

```javascript
var optionTag = $('option[value="foo"]');
```

### Section 2: Getting the Text

Once you have selected the option tag, you can use the `text()` method to get the text inside the tag. This method takes no arguments and will return the text as a string.

For example, if you had the option tag from the previous section, you could get the text inside it with the following code:

```javascript
var optionText = optionTag.text();
```

### Section 3: Putting It All Together

Putting all of the above together, you can get the text from a specific option tag with the following code:

```javascript
var optionText = $('option[value="foo"]').text();
```

### Section 4: Other Methods

In addition to the `text()` method, there are other methods that can be used to get the text from an option tag. The `html()` method can be used to get the HTML inside the tag, while the `val()` method can be used to get the value of the tag.

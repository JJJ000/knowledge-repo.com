---
title: What is the syntax for adding the !important flag to a css rule using the .css() method?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can apply !important using .css() in Javascript by setting the property value as a string with `!important` appended at the end.
---

**Contents**

[TOC]

### 1. Syntax

The syntax for applying !important using .css() in Javascript is as follows:

```
$(selector).css("propertyName", "value !important");
```

### 2. Example

For example, to apply !important to the font-size property of a paragraph element with the id "myParagraph":

```
$("#myParagraph").css("font-size", "20px !important");
```

### 3. Caveats

It is important to note that !important can only be applied to styles set via the .css() method in Javascript. It cannot be used to override styles set in an external stylesheet.

### 4. Browser Support

The .css() method is supported by all modern browsers, including Chrome, Firefox, Safari, and Edge.

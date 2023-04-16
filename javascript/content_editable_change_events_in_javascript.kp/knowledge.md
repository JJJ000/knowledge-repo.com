---
title: Events triggered when content is changed in a 'contenteditable' element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `change` event is triggered when the content of an element with the `contenteditable` attribute is modified.
---

**Contents**

[TOC]

#### Event

The `change` event is fired when the content of an element with the `contenteditable` attribute has been modified.

#### Syntax

The syntax for the `change` event is as follows:

```
element.addEventListener("change", myFunction);
```

#### Example

In this example, the `change` event is used to log the content of an element with the `contenteditable` attribute to the console when it is modified:

```
<div contenteditable="true" id="myDiv">This is editable.</div>

<script>
  document.getElementById("myDiv").addEventListener("change", function() {
    console.log(this.innerHTML);
  });
</script>
```

#### Browser Support

The `change` event is supported in all major browsers, including Internet Explorer 11 and above.

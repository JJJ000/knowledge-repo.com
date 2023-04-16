---
title: What is the process for altering the title of a web page in real time?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The title of a web page can be changed dynamically using the document.title property in Javascript.
---

**Contents**

[TOC]

# Section 1: Get the Current Title

To get the current title of a web page, you can use the `document.title` property. This will return the current title of the page as a string.

# Section 2: Change the Current Title

To change the current title of a web page, you can use the `document.title` property and assign it a new value. For example, to change the title to "My New Title," you would use the following code:

```
document.title = "My New Title";
```

# Section 3: Dynamically Change the Title

To dynamically change the title of a web page, you can use a combination of JavaScript and HTML. For example, you can use a `<input>` element with an `onchange` event handler that updates the `document.title` property when the value of the `<input>` element changes.

# Section 4: Example

Here is an example of how to dynamically change the title of a web page using HTML and JavaScript:

```
<input type="text" id="titleInput" onchange="document.title = this.value;">
```

When the value of the `<input>` element with the `id` of "titleInput" is changed, the `document.title` property is updated with the new value.

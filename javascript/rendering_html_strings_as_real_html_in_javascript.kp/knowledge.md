---
title: How can I display an html string as actual html?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the innerHTML property to set the HTML string as the element`s content.
---

**Contents**

[TOC]

1. **Using a DOM Parser**

Using a DOM Parser, you can parse the HTML string and render it into a DOM tree. This allows you to manipulate the HTML string as you would with any other DOM elements.

2. **Using an HTML Element**

You can create an HTML element object and set its `innerHTML` property to the HTML string you want to render. Then you can append the element to the DOM tree.

3. **Using a Template Engine**

You can use a template engine such as Mustache or Handlebars to render the HTML string. This is a more efficient way to render HTML strings as it allows you to use variables and other logic to render the HTML.

4. **Using a Library**

You can use a library such as jQuery or React to render the HTML string. These libraries provide powerful tools to manipulate and render HTML strings.

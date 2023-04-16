---
title: An explanation of the html script tag with the type attribute set to "text/template" 
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: <script type=`text/template`> ... </script> is a script tag used to store JavaScript-based templates in an HTML document.
---

**Contents**

[TOC]

#### What is <script type = "text/template">?

<script type = "text/template"> is an HTML element that is used to store client-side templates. It can be used to store HTML markup and JavaScript code that can be used to generate HTML elements on the client-side. The content inside the script tag is not rendered by the browser and is instead used as a template for generating HTML elements.

#### What is the purpose of <script type = "text/template">?

The purpose of <script type = "text/template"> is to provide a way for developers to store and reuse HTML and JavaScript code for generating HTML elements on the client-side. This can be used to reduce the amount of code that needs to be written for generating HTML elements, as the code can be stored in the template and reused multiple times.

#### How is <script type = "text/template"> used?

<script type = "text/template"> is used in conjunction with client-side JavaScript libraries such as jQuery and Mustache.js. These libraries provide methods for accessing the content of the script tag and using it to generate HTML elements. For example, jQuery provides the .html() method which can be used to access the content of the script tag and generate HTML elements.

#### Advantages of using <script type = "text/template">

Using <script type = "text/template"> has several advantages. It allows developers to store HTML and JavaScript code in a single place, reducing the amount of code that needs to be written. It also makes it easier to maintain the code, as changes can be made in one place and the changes will be reflected everywhere the template is used. Finally, it makes it easier to share code, as the template can be shared between different projects.

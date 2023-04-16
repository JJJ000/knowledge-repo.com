---
title: The import statement cannot be used outside of a module, which has caused a syntaxerror
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Import statements must be used within a module or script file in Javascript.
---

**Contents**

[TOC]

#Solution 

##Introduction
In Javascript, the `import` statement is used to import functions, objects, or a module from an external file. It is not possible to use the `import` statement outside a module, as it is a part of the module system.

##Reason
The `import` statement is part of the ES6 module system, which is not supported in all browsers. Therefore, it is not possible to use the `import` statement outside a module, as the module system has to be enabled in order for it to work.

##Alternatives
In order to use functions, objects, or modules from an external file, there are a few alternatives that can be used. The `require()` function can be used to import modules, the `<script>` tag can be used to include external scripts, and the `<link>` tag can be used to include external stylesheets.

##Conclusion
In conclusion, the `import` statement cannot be used outside a module in Javascript, as it is part of the ES6 module system which is not supported in all browsers. However, there are alternatives that can be used to include external files in a Javascript project.

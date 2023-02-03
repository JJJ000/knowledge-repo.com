---
title: The variable $ has not been declared or assigned a value
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: $ is a commonly used shorthand for jQuery, which is a JavaScript library that must be included in the code in order for $ to be defined.
---

**Contents**

[TOC]

# Overview
The Uncaught ReferenceError: $ is not defined error in Javascript occurs when attempting to call the `$` symbol, which is most commonly associated with jQuery, without first loading the jQuery library. This error indicates that the code is trying to use jQuery, but it is not loaded and thus not available for use.

# Causes
The most common cause of this error is attempting to use jQuery without first loading the jQuery library. This can occur if the library is not included in the web page before the code that is attempting to use jQuery is executed. It can also occur if the code is executing in a different context than the one in which jQuery was loaded.

# Solutions
The most straightforward solution to this error is to ensure that the jQuery library is loaded before any code that attempts to use jQuery is executed. This can be done by including the jQuery library in the HTML of the web page, or by using a script tag to load the library from a CDN.

Another possible solution is to use a library such as Lodash or Underscore, which provide similar functionality as jQuery, but do not require the jQuery library to be loaded.

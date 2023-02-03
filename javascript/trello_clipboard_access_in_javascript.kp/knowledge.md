---
title: What methods does trello use to access the contents of a user's clipboard?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Trello accesses the user`s clipboard in Javascript by using the navigator.clipboard API.
---

**Contents**

[TOC]

**Using the Clipboard API**

The Clipboard API provides the ability to access the user's clipboard in Javascript. This API is supported in most modern browsers, including Chrome, Firefox, and Safari. The Clipboard API allows developers to access the user's clipboard, read and write data to it, and even create new clipboard items.

**Using the execCommand Method**

The execCommand method is a method available in the document object that allows developers to access the user's clipboard. This method takes two parameters: the command to execute and the value to store in the clipboard. With the execCommand method, developers can copy, cut, and paste data from the user's clipboard.

**Using the document.execCommand Method**

The document.execCommand method is a method available in the document object that allows developers to access the user's clipboard. This method takes two parameters: the command to execute and the value to store in the clipboard. With the document.execCommand method, developers can copy, cut, and paste data from the user's clipboard.

**Using the ClipboardEvent Object**

The ClipboardEvent object is an object available in the document object that allows developers to access the user's clipboard. This object takes two parameters: the type of event and the data to store in the clipboard. With the ClipboardEvent object, developers can copy, cut, and paste data from the user's clipboard.

---
title: The window.location.href method in JavaScript allows the user to get the href (url) of the current page, while the window.open() method allows the user to open a new browser window or tab
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: window.location.href is used to get or set the current URL of the web page, while window.open() is used to open a new browser window.
---

**Contents**

[TOC]

# window.location.href

The window.location.href property returns the href (URL) of the current page. It also sets the href attribute of the location object.

Syntax:

window.location.href

Example:

window.location.href = "https://www.example.com";

# window.open ()

The window.open () method is used to open a new browser window or a tab.

Syntax:

window.open(URL, name, specs, replace)

Parameters:

URL: Required. Specifies the URL of the page to open.

name: Optional. Specifies the target attribute or the name of the window.

specs: Optional. A string that specifies the various window features to be included in the popup window (like status bar, address bar etc).

replace: Optional. A Boolean value, which specifies whether the URL creates a new entry or replaces the current entry in the history list.

Example:

window.open("https://www.example.com", "_blank", "toolbar=yes,scrollbars=yes,resizable=yes,top=500,left=500,width=400,height=400");

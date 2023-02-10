---
title: How can you display the content of a JSON response in html without showing the html tags to the user in angular 2?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the innerHTML property to set the HTML content of an element from a JSON response without displaying the tags to the user.
---

**Contents**

[TOC]

# Option 1: Sanitize HTML

Using the [DomSanitizer](https://angular.io/api/platform-browser/DomSanitizer) service from Angular, you can sanitize the HTML from a JSON response so that it is rendered properly in the browser without displaying the tags to the user.

# Option 2: Use a Directive

You can also create a custom directive to render the HTML from a JSON response without displaying the tags to the user. This directive can be used to parse the JSON response and render the HTML in the browser.

# Option 3: Use a Pipe

You can also create a custom pipe to render the HTML from a JSON response without displaying the tags to the user. This pipe can be used to parse the JSON response and render the HTML in the browser.

# Option 4: Use a Library

You can also use a library such as [Angular-sanitize](https://www.npmjs.com/package/angular-sanitize) to render the HTML from a JSON response without displaying the tags to the user. This library can be used to parse the JSON response and render the HTML in the browser.

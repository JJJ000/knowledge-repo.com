---
title: How can I show a JSON representation instead of [object object] on the screen?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON.stringify() method to convert the JSON object into a string representation.
---

**Contents**

[TOC]

**Section 1: Stringify JSON**

The simplest way to display a JSON representation on the screen is to use the `JSON.stringify()` method. This method takes a JavaScript object and converts it into a string representation of the object.

**Section 2: Logging to the Console**

Once the object has been stringified, it can be logged to the console using `console.log()`. This will display the JSON representation in the console, making it easier to read and debug.

**Section 3: Rendering in the Browser**

If the JSON representation needs to be displayed in the browser, it can be rendered using the `document.write()` method. This will output the stringified JSON representation on the page.

**Section 4: Formatting the Output**

The output of the `JSON.stringify()` method can be formatted for easier readability by passing the `space` argument. This argument takes a number or string that will be used to indent the output. For example, `JSON.stringify(obj, null, 2)` will output the JSON representation with two spaces of indentation.

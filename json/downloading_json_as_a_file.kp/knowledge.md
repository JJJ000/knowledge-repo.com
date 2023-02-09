---
title: Save a JSON object as a file in the browser
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the browser`s built-in `Save As` functionality to download a JSON object as a file.
---

**Contents**

[TOC]

# Section 1: Using JavaScript

Using JavaScript, you can easily download a JSON object as a file from the browser. To do this, you will need to create a Blob object from the JSON object, create a link element, set the href attribute of the link element to the Blob object, and finally use the click() method to trigger the download.

# Section 2: Creating a Blob Object

The first step is to create a Blob object from the JSON object. This can be done by using the Blob constructor and passing in the JSON object as an argument. The Blob constructor takes two arguments, the first one being the data, and the second one being an object containing the type of data.

# Section 3: Creating a Link Element

The next step is to create a link element. This can be done using the document.createElement() method and passing in the string “a” as the argument.

# Section 4: Setting the Link Element's Attributes

Once the link element has been created, the next step is to set the href attribute of the link element to the Blob object. This can be done using the setAttribute() method and passing in the string “href” as the first argument and the Blob object as the second argument.

Finally, the click() method can be used to trigger the download. This can be done by calling the click() method on the link element.

---
title: What is the best way to use javascript/jquery to get the content of an iframe?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can access the contents of an iframe with JavaScript/jQuery by using the `contentWindow` property.
---

**Contents**

[TOC]

## Accessing the Iframe

The first step in accessing the contents of an iframe with JavaScript/jQuery is to get a reference to the iframe. This can be done by using the `document.getElementById()` method, which takes the id of the iframe as an argument.

```js
let iframe = document.getElementById("myIframe");
```

## Accessing the Iframe's Document

Once a reference to the iframe has been obtained, the next step is to access the document inside the iframe. This can be done by using the `iframe.contentDocument` property, which returns a reference to the iframe's document.

```js
let iframeDoc = iframe.contentDocument;
```

## Accessing the Elements Within the Iframe

Once a reference to the iframe's document has been obtained, the next step is to access the elements within the iframe. This can be done by using the `iframeDoc.getElementById()` method, which takes the id of the element as an argument.

```js
let element = iframeDoc.getElementById("myElement");
```

## Accessing the Element's Content

Once a reference to the element has been obtained, the next step is to access the content of the element. This can be done by using the `element.innerHTML` property, which returns the content of the element as a string.

```js
let content = element.innerHTML;
```

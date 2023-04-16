---
title: How to initiate a file download when clicking an html button or using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To trigger a file download when clicking an HTML button or JavaScript, use the `download` attribute on the <a> tag.
---

**Contents**

[TOC]

## HTML

1. Create an `<a>` element with the `download` attribute set to the name of the file you want to download:

```html
<a href="path/to/file.pdf" download="file-name.pdf">Download File</a>
```

2. Add an event listener to the `<a>` element that triggers the click event when the HTML button is clicked:

```html
<button onclick="document.getElementById('downloadLink').click()">Download File</button>
```

## JavaScript

1. Create an `<a>` element with the `download` attribute set to the name of the file you want to download:

```js
const downloadLink = document.createElement('a');
downloadLink.href = 'path/to/file.pdf';
downloadLink.download = 'file-name.pdf';
```

2. Add an event listener to the `<a>` element that triggers the click event when the HTML button is clicked:

```js
document.querySelector('button').addEventListener('click', () => {
  downloadLink.click();
});
```

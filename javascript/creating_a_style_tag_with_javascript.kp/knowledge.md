---
title: What is the syntax for creating a <style> tag using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the document.createElement() method to create a <style> tag with Javascript.
---

**Contents**

[TOC]

## Using document.createElement

The `document.createElement` method can be used to create a `<style>` tag with Javascript.

```javascript
let styleTag = document.createElement("style");
```

## Setting Attributes

The `setAttribute` method can be used to set the type attribute of the `<style>` tag.

```javascript
styleTag.setAttribute("type", "text/css");
```

## Adding Content

The `innerHTML` property can be used to add content to the `<style>` tag.

```javascript
styleTag.innerHTML = "h1 { color: red; }";
```

## Adding to the Document

The `appendChild` method can be used to add the `<style>` tag to the document.

```javascript
document.head.appendChild(styleTag);
```

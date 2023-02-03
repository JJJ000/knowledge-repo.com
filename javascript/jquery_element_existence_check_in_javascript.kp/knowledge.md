---
title: See if an element is present in jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: jQuery has the method `length` to check if an element exists.
---

**Contents**

[TOC]

1. Checking for Existence of an Element
--------------------------------------
The most common way to check for the existence of an element in jQuery is to use the `length` property. This property returns the number of elements that match the given selector. If the length is greater than 0, then the element exists. 

```js
if ($('#some-element').length) {
  // element exists
}
```

2. Checking for Visibility
--------------------------
In some cases, you may want to check if an element is visible on the page. To do this, you can use the `is()` method and pass in the `:visible` selector.

```js
if ($('#some-element').is(':visible')) {
  // element is visible
}
```

3. Checking for Existence and Visibility
----------------------------------------
You can also combine the two checks above to check for both existence and visibility of an element.

```js
if ($('#some-element').length && $('#some-element').is(':visible')) {
  // element exists and is visible
}
```

4. Checking for Existence and Visibility of Multiple Elements
-------------------------------------------------------------
You can also use the `length` and `is()` methods to check for the existence and visibility of multiple elements.

```js
if ($('.some-elements').length && $('.some-elements').is(':visible')) {
  // elements exist and are visible
}
```

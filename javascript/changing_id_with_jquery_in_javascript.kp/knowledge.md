---
title: Using jquery to modify an element's id
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery can be used to change an element`s ID by using the .attr() method.
---

**Contents**

[TOC]

1. Select the Element #
Using jQuery, the element can be selected by its ID by using the `$('#id')` selector.

2. Set the New ID #
The new ID can be set using the `attr()` method.

```js
$('#oldId').attr('id', 'newId');
```

3. Test the New ID #
To ensure that the new ID has been successfully set, the `attr()` method can be used to check the element's ID.

```js
$('#newId').attr('id'); // returns 'newId'
```

4. Use the New ID #
The new ID can now be used to select the element using the `$('#id')` selector.

```js
$('#newId'); // returns the element with the new ID
```

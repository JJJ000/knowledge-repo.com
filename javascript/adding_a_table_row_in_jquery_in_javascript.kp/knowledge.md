---
title: Inserting a new row into a table using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery`s append() or appendTo() methods can be used to add a table row in jQuery.
---

**Contents**

[TOC]

## Adding a Table Row

Adding a table row to an existing table with jQuery is a simple task. Here are the steps to follow:

### Step 1: Create a New Table Row

First, create a new table row element and set its attributes. This can be done using the jQuery `.append()` method.

```js
var newRow = $('<tr>');
newRow.attr('id', 'newRow');
```

### Step 2: Add Cells to the Row

Next, add cells to the new row. This can be done using the jQuery `.append()` method.

```js
newRow.append('<td>Cell 1</td>');
newRow.append('<td>Cell 2</td>');
```

### Step 3: Add the Row to the Table

Finally, add the new row to the table. This can be done using the jQuery `.append()` method.

```js
$('#myTable').append(newRow);
```

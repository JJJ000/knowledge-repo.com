---
title: How can I use jquery to delete a row from a table?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The best way to remove a table row with jQuery in Javascript is to use the jQuery .remove() method.
---

**Contents**

[TOC]

## Using `.remove()`
The `.remove()` method can be used to remove a table row from an HTML table. This method takes no arguments and can be used on any jQuery object that contains a table row element.

## Example
The following example demonstrates how to use the `.remove()` method to remove a table row from an HTML table:

```javascript
$("#myTable tr:last").remove();
```

This example will remove the last row from the table with the ID of `myTable`.

## Removing Multiple Rows
To remove multiple table rows from an HTML table, the `.remove()` method can be used in a loop. The following example demonstrates how to remove all table rows from an HTML table:

```javascript
$("#myTable tr").each(function() {
    $(this).remove();
});
```

## Removing Specific Rows
To remove specific table rows from an HTML table, the `.remove()` method can be used in combination with other jQuery selectors. The following example demonstrates how to remove all table rows with the class `myClass` from an HTML table:

```javascript
$("#myTable tr.myClass").remove();
```

---
title: Constructing table rows in jquery from an ajax response in JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Using the jQuery .each() method, you can loop through the AJAX response (JSON) and create table rows with the data.
---

**Contents**

[TOC]

## 1. Parse JSON

Using the `$.getJSON()` method, the JSON data can be retrieved and parsed.

```js
$.getJSON('url', function(data) {
  // parse data here
});
```

## 2. Loop Through Data

Using a `for` loop, we can loop through the data and build the table rows.

```js
for (var i=0; i < data.length; i++) {
  // build table row here
}
```

## 3. Build Table Row

Using jQuery, we can build the table row and add it to the table.

```js
var row = $('<tr>');
row.append($('<td>').text(data[i].name));
row.append($('<td>').text(data[i].age));
row.append($('<td>').text(data[i].city));
$('#table').append(row);
```

## 4. Display Table

Finally, we can display the table by calling the `$('#table').show()` method.

```js
$('#table').show();
```

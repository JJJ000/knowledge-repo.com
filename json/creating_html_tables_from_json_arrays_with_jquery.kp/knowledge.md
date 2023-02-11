---
title: Transform a JSON array into a html table using jquery
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: jQuery can be used to convert a JSON array into an HTML table by looping through the array and appending the HTML table row elements.
---

**Contents**

[TOC]

# Section 1: HTML Table

Create an HTML table with the appropriate number of columns and rows. Include a `<thead>` element with `<th>` elements for the column headers and a `<tbody>` element with `<td>` elements for the data.

# Section 2: jQuery

Create a jQuery function that takes the JSON array as a parameter. Use a `$.each()` loop to iterate over the array, and use `$('#tableID').append()` to add the data to the HTML table.

# Section 3: JSON Array

Create a JSON array with the appropriate data. Include a `key` for each column header and a `value` for each row.

# Section 4: Initialization

Call the jQuery function with the JSON array as the parameter to initialize the table.

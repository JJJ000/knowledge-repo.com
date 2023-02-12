---
title: Change JSON into a datatable
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The Newtonsoft.Json library can be used to deserialize a JSON string into a DataTable object.
---

**Contents**

[TOC]

1. What is JSON? 
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays (called objects).

2. What is a DataTable? 
A DataTable is an in-memory representation of structured data. It is a collection of rows and columns of data that can be bound to a UI element such as a DataGridView. It is typically used to store and manipulate data in an application.

3. How to Convert JSON to DataTable? 
The process of converting JSON to a DataTable involves deserializing the JSON string into an object, looping through the object's properties, and adding each property to a DataTable. The process can be done manually or by using a library such as Newtonsoft.Json.

4. Benefits of Converting JSON to DataTable 
Converting JSON to a DataTable provides a number of benefits, including the ability to bind the data to a UI element such as a DataGridView, the ability to manipulate the data more easily, and the ability to query the data using SQL. Additionally, the data can be easily exported to other formats such as CSV and Excel.

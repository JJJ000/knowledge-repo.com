---
title: Change mongoose documents into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Mongoose documents can be converted to JSON using the .toJSON() method.
---

**Contents**

[TOC]

## Using Mongoose to Convert Documents to JSON

Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It provides a straight-forward, schema-based solution to model your application data. Mongoose also provides a convenient way to convert documents to JSON. 

## Retrieving Documents

To convert documents to JSON, you must first retrieve the documents from the database. You can do this using the `find()` method in Mongoose. This method takes a query object as a parameter, which can be used to specify the documents you want to retrieve.

## Converting Documents to JSON

Once you have retrieved the documents, you can use the `toJSON()` method to convert them to JSON. This method takes no parameters and returns a JSON object representing the document.

## Example

The following example shows how to use the `find()` and `toJSON()` methods to retrieve and convert documents to JSON.

```js
// Retrieve documents from the database
const docs = await Model.find({ /* query */ });

// Convert documents to JSON
const jsonDocs = docs.map(doc => doc.toJSON());
```

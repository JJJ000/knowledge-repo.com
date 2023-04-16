---
title: What is the process for updating or inserting a new document using mongoose?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Model.updateOne() or Model.updateMany() methods to update/upsert documents in Mongoose.
---

**Contents**

[TOC]

## Update Document

To update a document in Mongoose, you can use the `Model.update()` method. This method takes two parameters, a query object and an update object. The query object is used to specify which documents you want to update, and the update object is used to specify the changes you want to make.

For example, to update a document with the name “John” to have an age of 20, you can use the following code:

```javascript
Model.update({name: 'John'}, {$set: {age: 20}});
```

## Upsert Document

To upsert a document in Mongoose, you can use the `Model.update()` method with the {upsert: true} option. This will create a new document if one does not already exist with the specified query parameters.

For example, to upsert a document with the name “John” and an age of 20, you can use the following code:

```javascript
Model.update({name: 'John'}, {$set: {age: 20}}, {upsert: true});
```

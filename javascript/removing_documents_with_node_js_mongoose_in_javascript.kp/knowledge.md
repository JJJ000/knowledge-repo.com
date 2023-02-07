---
title: What is the process for deleting documents using Node.js mongoose?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Model.deleteOne() or Model.deleteMany() methods.
---

**Contents**

[TOC]

## Delete a Single Document

To delete a single document using Node.js Mongoose, we can use the `Model.findOneAndDelete()` method. This method takes two arguments: a query object and a callback function. The query object is used to find the document to delete and the callback function is used to handle the result of the operation.

Example: 
```javascript
User.findOneAndDelete({name: 'John'}, function(err, doc) {
  if (err) {
    console.log(err);
  } else {
    console.log(doc);
  }
});
```

## Delete Multiple Documents

To delete multiple documents using Node.js Mongoose, we can use the `Model.deleteMany()` method. This method takes two arguments: a query object and a callback function. The query object is used to find the documents to delete and the callback function is used to handle the result of the operation.

Example: 
```javascript
User.deleteMany({name: 'John'}, function(err, docs) {
  if (err) {
    console.log(err);
  } else {
    console.log(docs);
  }
});
```

## Delete All Documents

To delete all documents using Node.js Mongoose, we can use the `Model.deleteMany()` method with an empty query object. This method takes two arguments: a query object and a callback function. The empty query object will match all documents in the collection and the callback function is used to handle the result of the operation.

Example: 
```javascript
User.deleteMany({}, function(err, docs) {
  if (err) {
    console.log(err);
  } else {
    console.log(docs);
  }
});
```

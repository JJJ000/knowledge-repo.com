---
title: How to change the name of a database field in an array in mongodb?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the positional operator ($) along with the $rename operator to rename fields within an array in MongoDB.
---

**Contents**

[TOC]

## Introduction

In MongoDB, we can easily rename a database field within an array in JSON. This can be done using the `$rename` operator. In this tutorial, we will discuss how to do it step by step.


## Prerequisites

Before continuing, make sure you have the following installed:

- MongoDB server.
- MongoDB client.


## Steps to Rename a Database Field within an Array in JSON

1. Connect to the MongoDB server using the MongoDB client.
2. Select the database that contains the collection with the array.
3. Use the `$rename` operator on the array field to rename the database field within the array.
4. Specify the new name of the database field within the array as the value of the `$rename` operator.


## Step-by-Step Guide

1. Connect to the MongoDB server using the MongoDB client.

```
mongo
```

2. Select the database that contains the collection with the array.

```
use testdb
```

3. Use the `$rename` operator on the array field to rename the database field within the array.

```
db.testcol.update(
  {}, // Select all documents in the collection.
  { $rename: { "arrayfield.oldname": "arrayfield.newname" } }, // Rename the field within the array.
  false, // Upsert: don't create new documents if none match the query.
  true // Multi: update all matching documents.
);
```

4. Specify the new name of the database field within the array as the value of the `$rename` operator.

After running this command, the database field within the array named "oldname" will be renamed to "newname".

That's it! You have successfully renamed a database field within an array in JSON using the `$rename` operator in MongoDB.

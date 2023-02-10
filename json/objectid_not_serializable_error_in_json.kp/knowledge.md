---
title: Objectid() cannot be converted into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: ObjectIds cannot be serialized to JSON.
---

**Contents**

[TOC]

## What is ObjectId?
ObjectId is a 12-byte BSON type used to uniquely identify documents within a collection in MongoDB. It is typically used as the value of the _id field of documents in MongoDB.

## What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based format that is used to store and exchange data, and is based on a subset of the JavaScript programming language.

## Why is ObjectId not JSON Serializable?
ObjectId is not serializable in JSON because it is not a valid JSON type. JSON only supports a limited set of data types, including strings, numbers, booleans, arrays, and objects. ObjectId is not one of these types, so it cannot be serialized in JSON.

## How to Serialize ObjectId in JSON?
ObjectId can be serialized in JSON by converting it to a string. To do this, use the toString() method on the ObjectId object. This will return a string representation of the ObjectId that can then be serialized in JSON.

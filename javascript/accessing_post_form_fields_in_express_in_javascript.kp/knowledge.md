---
title: What is the process for retrieving data from post form fields in express?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: In Express, POST form fields can be accessed using the req.body object.
---

**Contents**

[TOC]

1. **Including the body-parser Middleware**

Before you can access POST form fields in Express, you must include the body-parser middleware in your Express application. This middleware is responsible for parsing the incoming request body and making it available as req.body.

2. **Retrieving POST Form Fields**

Once you have included the body-parser middleware, you can retrieve POST form fields from the req.body object. The req.body object is a JavaScript object that contains all the form fields submitted in the request.

3. **Accessing Form Fields**

You can access individual form fields using the dot notation. For example, if you have a form field called ‘name’, you can access its value using req.body.name.

4. **Handling Form Submissions**

Once you have retrieved the form fields, you can use them to handle the form submission. You can use the form fields to store data in a database, send an email, or whatever you need to do with the form data.

---
title: What is the process for getting the request payload?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The request payload can be retrieved from the request body using the json() method.
---

**Contents**

[TOC]

# Section 1: Retrieve Request Payload in Node.js

In Node.js, the request payload can be retrieved by using the `body-parser` middleware. This middleware parses the incoming request and makes the payload available in `req.body`.

# Section 2: Install body-parser

The `body-parser` middleware must be installed before it can be used. This can be done using the `npm` command:

```
npm install body-parser
```

# Section 3: Use body-parser

Once the `body-parser` middleware is installed, it can be used in the Node.js application by requiring it and adding it to the Express app:

```
const bodyParser = require('body-parser');

app.use(bodyParser.json());
```

# Section 4: Access Request Payload

Once the `body-parser` middleware is added, the request payload can be accessed in the Express application by using the `req.body` object. For example, if the request payload is a JSON object, it can be accessed like this:

```
const data = req.body;
```

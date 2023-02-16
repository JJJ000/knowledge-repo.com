---
title: What is the purpose of using the bodyparser.json() function in the app.use() method?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: It parses incoming requests with JSON payloads and is based on body-parser.
---

**Contents**

[TOC]

#### What is bodyParser?
BodyParser is a middleware used to parse incoming request bodies in a middleware before your handlers, available under the req.body property.

#### What does bodyParser.json() do?
bodyParser.json() parses the body of an incoming request and makes it available as a JavaScript object. It is specifically used to parse JSON data from the request body.

#### What does app.use() do?
app.use() is a function in Express that allows you to register middleware. Middleware is a function that is invoked by Express before the request handler.

#### What does app.use(bodyParser.json()) do?
app.use(bodyParser.json()) registers the bodyParser middleware with Express and enables it to parse JSON data from the request body.

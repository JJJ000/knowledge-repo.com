---
title: The difference between express.json and bodyparser.json is that express.json is a built-in middleware function in express, while bodyparser.json is a Node.js module that parses the body of an incoming request
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Express.json is a built-in middleware function in Express.js that parses incoming request bodies in a middleware before your handlers, whereas bodyParser.json is a third-party middleware package that does the same thing.
---

**Contents**

[TOC]

### express.json
Express.json is a built-in middleware function in Express. It parses incoming requests with JSON payloads and is based on body-parser. It exposes the parsed data on req.body.

### bodyParser.json
bodyParser.json is a Node.js body parsing middleware. It parses incoming requests with JSON payloads and exposes the parsed data on req.body. It is based on the native JSON.parse() function.

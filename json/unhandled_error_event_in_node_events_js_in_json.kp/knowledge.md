---
title: An 'error' event is thrown on node events.js line 167 that is not being handled
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: An unhandled `error` event in Json will cause an error to be thrown.
---

**Contents**

[TOC]

## What is an Unhandled 'error' Event?
An unhandled 'error' event is an event that is triggered when an error occurs in a Node.js application. The event is emitted when an error is not caught and handled by the application.

## What Causes an Unhandled 'error' Event in Json?
An unhandled 'error' event in Json can be caused by a number of things. These can include invalid Json syntax, missing fields, or incorrect data types.

## How to Handle an Unhandled 'error' Event in Json
The best way to handle an unhandled 'error' event in Json is to wrap the code that is generating the event in a try/catch block. This will allow the application to catch and handle any errors that may occur.

## How to Avoid an Unhandled 'error' Event in Json
To avoid an unhandled 'error' event in Json, it is important to ensure that all of the data being passed into the application is valid and properly formatted. Additionally, it is important to use the appropriate data types for the data being passed in.

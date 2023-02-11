---
title: Using <%= with express and ejs to output a json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Yes, ejs with <%= can be used to render a JSON in HTML.
---

**Contents**

[TOC]

## Section 1: Express
Express is a Node.js web application framework that provides a robust set of features for web and mobile applications. It is the de facto standard server framework for Node.js.

## Section 2: EJS
EJS (Embedded JavaScript) is a simple templating language that lets you generate HTML markup with plain JavaScript. It can be used in combination with Express to render dynamic web pages.

## Section 3: Rendering JSON
JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to exchange data between a server and a client. Express and EJS can be used together to render JSON data in a web page.

## Section 4: Using <%=
The <%= tag in EJS is used to output the value of a given expression. It can be used to render a JSON object in the page. For example, to render a JSON object in the page, you can use the following code:

<%= JSON.stringify(jsonObject) %>

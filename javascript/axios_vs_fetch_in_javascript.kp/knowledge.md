---
title: What are the distinctions between axios and fetch?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Axios is a promise-based HTTP client for the browser and Node.js, while Fetch is an API for making web requests.
---

**Contents**

[TOC]

#### Axios
Axios is a JavaScript library used to make HTTP requests from node.js or XMLHttpRequests from the browser and it supports the Promise API that is native to JS ES6. It simplifies the process of making AJAX calls and also supports automatic transforming of JSON data.

#### Fetch
Fetch is an API that provides an interface for fetching resources. It is not dependent on a specific library or framework and can be used in plain JavaScript. It also uses Promises to provide a more straightforward way of handling asynchronous operations.

#### Differences
- Axios supports automatic transforming of JSON data while Fetch does not.
- Axios provides a more comprehensive feature set than Fetch, including automatic transformation of data, error handling, and support for older browsers.
- Fetch is more lightweight and can be used in plain JavaScript, while Axios requires the use of a library or framework.
- Fetch supports streaming, while Axios does not.

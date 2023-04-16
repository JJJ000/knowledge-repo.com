---
title: What is the best way to separate a url into its hostname and path components using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the URL API`s `URL.hostname` and `URL.pathname` properties to parse a URL into hostname and path in JavaScript.
---

**Contents**

[TOC]

**Section 1: Extract the URL**

The first step is to extract the URL string from the source. Depending on the source, this could be done in various ways. For example, if the URL is part of a string, it could be extracted using the `String.prototype.match()` method.

**Section 2: Parse the URL**

The next step is to parse the URL. This can be done using the `URL` constructor. The constructor takes the URL string as its parameter and returns an object containing various properties related to the URL.

**Section 3: Extract the Hostname**

The hostname can be extracted from the URL object using the `hostname` property. This property returns the hostname of the URL.

**Section 4: Extract the Path**

The path can be extracted from the URL object using the `pathname` property. This property returns the path of the URL.

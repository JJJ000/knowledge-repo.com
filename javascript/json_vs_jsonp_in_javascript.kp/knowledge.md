---
title: How do JSON and jsonp differ?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: JSON is a data format, while JSONP is a technique used to make cross-domain requests using a script tag.
---

**Contents**

[TOC]

**JSON**

- Data Format:
  JSON is a text-based data format that uses JavaScript Object Notation (JSON) to store and exchange data. It is a lightweight, language-independent data interchange format.

- Security:
  JSON is a secure format, as it does not allow for cross-domain requests. This means that data can only be accessed by the same domain that is hosting the data.

**JSONP**

- Data Format:
  JSONP is a script tag-based data format that uses JavaScript Object Notation (JSON) to store and exchange data. It is a lightweight, language-independent data interchange format.

- Security:
  JSONP is an insecure format, as it allows for cross-domain requests. This means that data can be accessed by any domain, even if it is not hosting the data.

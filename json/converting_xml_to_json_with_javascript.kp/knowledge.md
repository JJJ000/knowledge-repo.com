---
title: Transform xml into JSON and vice versa using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Using the built-in JSON.stringify() and JSON.parse() functions, you can easily convert XML to JSON and back in Javascript.
---

**Contents**

[TOC]

# Section 1: Converting XML to JSON

The easiest way to convert XML to JSON using JavaScript is to use the `xml2json` library. This library is available on npm and can be installed using the following command:

`npm install xml2json`

Once installed, it can be used to convert XML to JSON using the following code:

```javascript
const xml2json = require('xml2json');
const xml = '<root>...</root>';
const json = xml2json.toJson(xml);
```

# Section 2: Converting JSON to XML

The `xml2json` library can also be used to convert JSON to XML. This can be done using the following code:

```javascript
const xml2json = require('xml2json');
const json = { ... };
const xml = xml2json.toXml(json);
```

# Section 3: Other Libraries

There are several other libraries available for converting XML to JSON and vice versa. Some of the more popular libraries include `xml-js`, `json2xml`, and `xml-parser`.

# Section 4: Manual Conversion

It is also possible to manually convert XML to JSON and vice versa. For example, the following code can be used to convert XML to JSON:

```javascript
const xml2json = require('xml2js');
const xml = '<root>...</root>';
const json = xml2js.parseStringSync(xml);
```

Similarly, the following code can be used to convert JSON to XML:

```javascript
const xml2js = require('xml2js');
const json = { ... };
const xml = xml2js.buildObjectSync(json);
```

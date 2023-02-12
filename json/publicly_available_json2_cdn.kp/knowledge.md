---
title: Is there a cdn that is accessible to the public and provides hosting for json2?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, JSON2 can be found hosted on the cdnjs CDN.
---

**Contents**

[TOC]

## CDN Hosts

JSON2 is available on several Content Delivery Networks (CDNs), including:

* [jsDelivr](https://www.jsdelivr.com/package/npm/json2)
* [UNPKG](https://unpkg.com/json2@2.5.0/lib/json2.js)
* [CDNJS](https://cdnjs.com/libraries/json2)

## Usage

Using any of the above CDNs, you can include JSON2 in your HTML or JavaScript code as follows:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/json2/2.5.0/json2.min.js"></script>
```

Or, if you are using a module bundler such as Webpack or Browserify:

```js
import json2 from 'https://cdnjs.cloudflare.com/ajax/libs/json2/2.5.0/json2.min.js';
```

## License

JSON2 is released under the [MIT license](https://github.com/douglascrockford/JSON-js/blob/master/LICENSE).

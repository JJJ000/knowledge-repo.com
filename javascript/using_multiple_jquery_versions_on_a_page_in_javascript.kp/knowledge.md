---
title: Is it possible to have more than one version of jquery on the same page?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Yes, you can use multiple versions of jQuery on the same page in Javascript.
---

**Contents**

[TOC]

## Yes

Yes, it is possible to use multiple versions of jQuery on the same page in Javascript. This can be done by loading different versions of jQuery into different script tags, or by using a jQuery migration plugin.

## Script Tags

The simplest way to use multiple versions of jQuery on the same page is to load them into separate script tags. This can be done by creating two script tags, with each one pointing to a different version of jQuery. For example:

```
<script src="https://code.jquery.com/jquery-1.12.4.js"></script>
<script src="https://code.jquery.com/jquery-2.2.4.js"></script>
```

## Migration Plugin

Another way to use multiple versions of jQuery on the same page is to use a jQuery migration plugin. This plugin allows you to load multiple versions of jQuery on the same page, and it will automatically detect which version of jQuery is being used and adjust the code accordingly. This can be a useful tool for developers who need to support multiple versions of jQuery on the same page.

## Conclusion

In conclusion, it is possible to use multiple versions of jQuery on the same page in Javascript. This can be done by loading different versions of jQuery into separate script tags, or by using a jQuery migration plugin.

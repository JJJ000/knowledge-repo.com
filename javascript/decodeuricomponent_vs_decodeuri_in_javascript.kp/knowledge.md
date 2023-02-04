---
title: How do decodeuricomponent and decodeuri differ?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: decodeURIComponent decodes all characters while decodeURI only decodes special characters.
---

**Contents**

[TOC]

**DecodeURIComponent**

DecodeURIComponent is a function in Javascript which is used to decode a URI component. It is used to decode a component of a URL which has been encoded using the encodeURIComponent() function. It decodes all characters except for the following: alphabetic, decimal digits, - _ . ! ~ * ' ( )

**DecodeURI**

DecodeURI is a function in Javascript which is used to decode a URI. It is used to decode a URL which has been encoded using the encodeURI() function. It decodes all characters except for the following: alphabetic, decimal digits, - _ . ! ~ * ' ( ) : @ & = + $ , / ? # [ ]

**Difference**

The main difference between decodeURIComponent and decodeURI is that decodeURIComponent decodes a single component of a URL while decodeURI decodes an entire URL. DecodeURIComponent is more specific and is used when only one component of a URL needs to be decoded. DecodeURI is used when an entire URL needs to be decoded.

---
title: What is the difference between using escape and encodeuri / encodeuricomponent?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You should use escape when encoding strings for use in a URL query string.
---

**Contents**

[TOC]

1. When Encoding Special Characters 
When special characters need to be encoded, such as spaces, quotes, or other characters that are not part of the standard ASCII set, escape() should be used instead of encodeURI() or encodeURIComponent().

2. When Encoding Non-ASCII Characters 
When encoding non-ASCII characters, such as Chinese, Japanese, or Korean characters, escape() should be used instead of encodeURI() or encodeURIComponent().

3. When Encoding URLs 
When encoding URLs, encodeURI() should be used instead of escape() or encodeURIComponent().

4. When Encoding Query Strings
When encoding query strings, encodeURIComponent() should be used instead of escape() or encodeURI().

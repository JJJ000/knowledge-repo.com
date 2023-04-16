---
title: Detecting browser language preference using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The navigator.languages property can be used to detect the browser language preference in JavaScript.
---

**Contents**

[TOC]

# Section 1: Get Language Preference

The `navigator.language` property can be used to get the language preference of the browser. It returns a string with a two-letter language code, such as "en" for English.

# Section 2: Detect Language

The language preference can be used to detect the language of the browser. This can be done by comparing the language code with a list of supported languages. If the language code matches a language in the list, then the language is detected.

# Section 3: Fallback Language

If the language preference is not supported, then a fallback language can be used. This can be a language that is supported by the website or app, or a default language such as English.

# Section 4: Store Language Preference

The language preference can be stored in a cookie or local storage so that it can be used in future visits. This allows the website or app to remember the user's language preference and use it when displaying content.

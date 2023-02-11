---
title: Handling special characters in bash scripts for json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: In bash, escaping characters in JSON requires the use of backslashes (\) before the character to be escaped.
---

**Contents**

[TOC]

# Escaping Single Quotes

Single quotes can be escaped in JSON by using a backslash `\` before the single quote. For example, `'This is a \'single quote\''` will be rendered as `"This is a 'single quote'"` in JSON.

# Escaping Double Quotes

Double quotes can be escaped in JSON by using a backslash `\` before the double quote. For example, `"This is a \"double quote\""` will be rendered as `"This is a "double quote""` in JSON.

# Escaping Backslashes

Backslashes can be escaped in JSON by using a double backslash `\\` before the backslash. For example, `"This is a \\backslash\\"` will be rendered as `"This is a \backslash\"` in JSON.

# Escaping Special Characters

Special characters can be escaped in JSON by using a backslash `\` before the character. For example, `"This is a \n new line"` will be rendered as `"This is a \n new line"` in JSON.

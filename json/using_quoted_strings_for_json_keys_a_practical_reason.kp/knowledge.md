---
title: What is the benefit of using quoted strings for JSON keys?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, quoted strings are not necessary for JSON keys, as long as they are valid identifiers.
---

**Contents**

[TOC]

1. **Readability:** Quoted strings make it easier to read keys in JSON. This is especially useful when the key is a long string or contains special characters.

2. **Compatibility:** Quoted strings are compatible with most JSON parsers, whereas unquoted strings may not be.

3. **Uniformity:** Quoting all keys in a JSON object ensures a uniform look, making it easier to spot potential errors.

4. **Security:** Quoted strings can be used to prevent malicious code from being injected into JSON objects. This can prevent security vulnerabilities such as cross-site scripting (XSS) attacks.

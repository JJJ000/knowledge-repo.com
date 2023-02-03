---
title: A password must have at least 8 characters, including at least one number, one lowercase letter, one uppercase letter, and one special character, for it to be valid according to the regex
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$/
---

**Contents**

[TOC]

##### Regex
`/^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&])[A-Za-z\d@$!%*#?&]{8,}$/`

##### Explanation

`/^` - Start of the regex

`(?=.*[A-Za-z])` - Positive lookahead that asserts at least one letter

`(?=.*\d)` - Positive lookahead that asserts at least one number

`(?=.*[@$!%*#?&])` - Positive lookahead that asserts at least one special character

`[A-Za-z\d@$!%*#?&]{8,}` - Matches any combination of letters, numbers, and special characters of length 8 or more

`$/` - End of the regex

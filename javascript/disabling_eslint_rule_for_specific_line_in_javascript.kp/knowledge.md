---
title: Disabling an eslint rule for a particular line
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can turn off an eslint rule for a specific line by adding a comment with `eslint-disable-line` followed by the rule name.
---

**Contents**

[TOC]

#### Using Comments 

You can turn off a specific ESLint rule by adding a comment at the end of the line. The comment should be in the format `// eslint-disable-line <rule-name>`. 

For example, if you want to turn off the rule `no-unused-vars`, write the following line of code:

```js
let unusedVar; // eslint-disable-line no-unused-vars
```

#### Using Configuration Files

You can also turn off a specific ESLint rule by adding the rule name to the `rules` section of your ESLint configuration file. The rule should be set to `off` or `0`. 

For example, if you want to turn off the rule `no-unused-vars`, add the following line to your configuration file:

```
"no-unused-vars": 0
```

#### Using Inline Disabling 

You can also turn off a specific ESLint rule for a single line of code by using the `eslint-disable` directive. The directive should be in the format `/* eslint-disable <rule-name> */`. 

For example, if you want to turn off the rule `no-unused-vars` for a single line of code, write the following line of code:

```js
/* eslint-disable no-unused-vars */
let unusedVar;
/* eslint-enable no-unused-vars */
```

#### Using Global Disabling 

You can also turn off all ESLint rules for a specific line of code by using the `eslint-disable-line` directive. The directive should be in the format `// eslint-disable-line`.

For example, if you want to turn off all ESLint rules for a single line of code, write the following line of code:

```js
// eslint-disable-line
let unusedVar;
```

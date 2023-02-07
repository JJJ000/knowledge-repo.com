---
title: What is the source of this error message - "fatal error unable to find local grunt"?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: This error is caused by a missing or incorrect installation of Grunt, a JavaScript task runner.
---

**Contents**

[TOC]

### Cause

This error is caused when the Grunt command line interface (CLI) is unable to find the local Grunt installation on the system.

### Resolution

The most common resolution to this error is to install the Grunt CLI globally on the system. This can be done by running the following command:

```
npm install -g grunt-cli
```

Once the Grunt CLI has been installed, the error should no longer appear. It is also important to ensure that the local Grunt installation is up to date. This can be done by running the following command:

```
npm update
```

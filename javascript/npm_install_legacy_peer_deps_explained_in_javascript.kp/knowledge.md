---
title: What is the exact purpose of the npm install --legacy-peer-deps command? when is it recommended to use it and what are some potential use cases?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Npm install --legacy-peer-deps is used to install all peer dependencies of a package, and is recommended when installing packages that have a lot of peer dependencies.
---

**Contents**

[TOC]

# What is npm install --legacy-peer-deps?
NPM install --legacy-peer-deps is a command that allows developers to install legacy peer dependencies of a package. This command ensures that the dependencies are installed in the correct version, as specified by the package's version range.

# When is it recommended?
It is recommended when a package requires legacy peer dependencies, which are dependencies that are not specified in the package.json file. For example, if a package requires a specific version of a library, but the package.json does not specify the version, then this command can be used to install the correct version.

# What's a potential use case in Javascript?
A potential use case in Javascript is when a package requires a specific version of a library, but the package.json does not specify the version. This command can be used to install the correct version of the library, ensuring that the package will work properly.

# What's the benefit?
The benefit of using this command is that it ensures that the dependencies are installed in the correct version, as specified by the package's version range. This helps to prevent compatibility issues between packages and libraries, ensuring that the package will work properly.

---
title: What does the "@" symbol signify in the name of an npm package?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `@` prefix on npm packages in Javascript indicates that the package is a scoped package, meaning it is published on the npm registry under an organization or user namespace.
---

**Contents**

[TOC]

# Prefix Meaning
The "@" prefix on npm packages in Javascript indicates that the package is a scoped package. Scoped packages are packages that are published under an organization or user account, and are typically used for private packages.

# Naming Convention
The "@" prefix is followed by the package creator's username, followed by a forward slash, followed by the package name. For example, if the package creator's username is "example-user" and the package name is "example-package", the package would be named "@example-user/example-package".

# Accessibility
Scoped packages are not accessible to the general public by default. To access a scoped package, the user must be logged in to the same npm account that the package was published under.

# Benefits
The primary benefit of scoped packages is that they allow package creators to keep their packages private. This can be especially beneficial for companies that want to keep their packages private or for developers who want to keep their packages private until they are ready for public release.

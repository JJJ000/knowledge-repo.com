---
title: It is recommended that you commit the lockfile created by npm, named package-lock.json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, it is recommended to commit the package-lock.json file in order to ensure that the exact dependencies are installed each time the project is built.
---

**Contents**

[TOC]

#### Yes

Committing the package-lock.json file to your version control system is recommended as it will help ensure that the exact same versions of each package are used across all environments. This can help prevent unexpected bugs and compatibility issues in production.

#### Why

The package-lock.json file contains detailed information about the exact versions of all packages and their dependencies that were installed. This allows you to easily reproduce the exact same environment in other places, such as on another machine or in a CI/CD pipeline.

#### Benefits

By committing the package-lock.json file, you can ensure that the exact same versions of each package are used across all environments. This can help prevent unexpected bugs and compatibility issues in production.

#### Conclusion

In conclusion, committing the package-lock.json file to your version control system is highly recommended as it can help prevent unexpected bugs and compatibility issues.

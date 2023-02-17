---
title: The composer is in the process of updating its dependencies while suspended
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Composer can hang while updating dependencies in Json due to a lack of memory or other system resources.
---

**Contents**

[TOC]

1. Check Your Internet Connection

Before attempting to troubleshoot any other issues, make sure that your internet connection is working properly. If your internet connection is unstable or slow, Composer may hang while attempting to download and install dependencies.

2. Check for Conflicting Packages

Sometimes, Composer may hang while attempting to resolve conflicts between packages. If this is the case, you will need to manually edit the composer.json file to remove any conflicting packages.

3. Check for Outdated Packages

If you are using outdated packages, Composer may hang while attempting to update them. Make sure that all of your packages are up to date before attempting to update them with Composer.

4. Check for Corrupted Files

If any of the files that Composer is attempting to download or update are corrupted, it may hang while attempting to process them. Try deleting any corrupted files and re-downloading them to see if this resolves the issue.

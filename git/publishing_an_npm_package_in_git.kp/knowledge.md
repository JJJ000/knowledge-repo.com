---
title: What is the process for publishing an npm package with distribution files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can publish an npm package with distribution files in Git by using the `npm publish` command.
---

**Contents**

[TOC]

#### Step 1: Create the Package

Begin by creating a package.json file at the root of your project. This file should contain the metadata of your package, such as the name, version, description, and license. Additionally, you should include the files that should be included in the npm package in the "files" array.

#### Step 2: Commit the Package

Once the package.json file is created, add it to your Git repository and commit it. This ensures that the package will be versioned and tracked by Git.

#### Step 3: Publish the Package

The next step is to publish the package to npm. You can do this by running the following command:

```
npm publish
```

This will publish your package to npm, and make it available for others to install.

#### Step 4: Push to Git

Finally, you should push the changes to your Git repository. This will ensure that the package is available for others to download and install.

---
title: How can I specify a branch or tag to be used when installing a package from a git url in a package.json?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can specify a branch or tag in a git URL in the `dependencies` section of a package.json file.
---

**Contents**

[TOC]

### Step 1: Add the Git URL

In the `package.json` file, add the git URL of the branch or tag that you want to depend on. This should be placed in the `dependencies` object like any other dependency:

```json
"dependencies": {
    "my-package": "git+https://github.com/username/my-package#branch-or-tag"
}
```

### Step 2: Install Dependencies

Once you have added the git URL to the `package.json` file, you need to install the dependencies. This can be done with the `npm install` command.

### Step 3: Verify Dependency

You can verify that the correct branch or tag is being used by running the `npm ls` command. This will list all the dependencies and their versions, including the branch or tag that is being used.

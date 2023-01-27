---
title: What steps do I need to take to prevent git from tracking changes to file permissions (chmod)?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git can be configured to ignore file mode changes with the core.filemode setting.
---

**Contents**

[TOC]

### Section 1 - Check Your Global Settings

Git will track file mode changes by default, however it can be configured to ignore them. To check if this is the case, run the following command:

```git
git config --get core.filemode
```

If the output is `true`, then file mode changes will be tracked.

### Section 2 - Configure to Ignore File Mode Changes

To configure Git to ignore file mode changes, run the following command:

```git
git config core.filemode false
```

This will set the `core.filemode` configuration option to `false`, which will tell Git to ignore file mode changes.

### Section 3 - Commit Changes

Once the configuration has been set, you need to commit the changes to make them take effect. To do this, run the following command:

```git
git commit -m "Ignore file mode changes"
```

This will commit the changes to the repository, and Git will now ignore file mode changes.

### Section 4 - Verify Changes

To verify that Git is now ignoring file mode changes, run the following command:

```git
git config --get core.filemode
```

If the output is `false`, then file mode changes will be ignored.

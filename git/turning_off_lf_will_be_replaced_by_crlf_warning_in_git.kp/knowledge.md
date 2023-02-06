---
title: How can I disable the "lf will be replaced by crlf" warning when using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can turn off the `LF will be replaced by CRLF` warning by setting the config core.safecrlf to false.
---

**Contents**

[TOC]

1. **Configure the core.autocrlf Setting**

Git has a configuration setting called `core.autocrlf` that can be used to control how Git handles line endings. To turn off the warning, you can configure this setting to `false`.

2. **Check Your Global Configuration**

To check your global configuration, run the following command:

```
git config --global --get core.autocrlf
```

3. **Set the Configuration**

If the output of the command is not `false`, you can set the configuration with the following command:

```
git config --global core.autocrlf false
```

4. **Verify the Configuration**

To verify that the configuration has been set, run the following command:

```
git config --global --get core.autocrlf
```

The output should be `false`.

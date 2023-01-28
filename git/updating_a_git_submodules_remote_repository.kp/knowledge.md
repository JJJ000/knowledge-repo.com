---
title: What steps are needed to update the remote repository associated with a git submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git submodule set-url <submodule> <new\_url>` to change the remote repository for a git submodule.
---

**Contents**

[TOC]

1. **Check the Current Remote Repository**

To check the current remote repository for a git submodule, use the command `git config --get submodule.<submodule_name>.url`. This will output the URL of the currently configured remote repository.

2. **Update the Submodule Configuration**

To update the remote repository for the submodule, run the command `git config submodule.<submodule_name>.url <new_url>`. This will update the submodule's configuration to point to the new remote repository.

3. **Push the Changes**

Once the submodule's configuration has been updated, the changes must be pushed to the parent repository. To do this, run the command `git push origin master`.

4. **Update the Submodule**

Finally, to ensure that the submodule is pointing to the new remote repository, run the command `git submodule update --remote <submodule_name>`. This will ensure that the submodule is pointing to the new remote repository.

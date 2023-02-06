---
title: Is it possible to configure git to automatically fetch all tags when performing a remote pull?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, it is not possible to set a Git default to fetch all tags during a remote pull.
---

**Contents**

[TOC]

## Yes

Git allows users to set a default to fetch all tags during a remote pull. This can be done by setting the `fetch.prune` configuration option to `false`.

## Setting the Configuration Option

The `fetch.prune` configuration option can be set using the `git config` command. This command can be used to set the configuration option to `false` for a single repository, or to all repositories on the local machine.

For a single repository:

```
git config fetch.prune false
```

For all repositories on the local machine:

```
git config --global fetch.prune false
```

## Verifying the Configuration Option

The `git config` command can also be used to verify that the `fetch.prune` configuration option is set to `false`.

For a single repository:

```
git config --get fetch.prune
```

For all repositories on the local machine:

```
git config --global --get fetch.prune
```

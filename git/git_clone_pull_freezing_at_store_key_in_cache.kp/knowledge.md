---
title: Git clone/pull keeps getting stuck at the prompt "store key in cache?"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Answer Press `n` to skip storing the key in the cache.
---

**Contents**

[TOC]

#### Solution 1

If the Git clone or pull continually freezes at "Store key in cache?", the best solution is to delete the SSH key from the ssh-agent cache. To do this, run the following command in the terminal:

```
ssh-add -D
```

#### Solution 2

Another solution is to use a different SSH key. To do this, generate a new SSH key by running the following command in the terminal:

```
ssh-keygen -t rsa -b 4096
```

Then, add the new SSH key to your GitHub account.

#### Solution 3

It is also possible to disable the SSH key caching by running the following command in the terminal:

```
git config --global credential.helper 'cache --timeout=0'
```

This will prevent Git from caching the SSH key and will allow you to clone or pull without freezing.

#### Solution 4

Finally, you can try disabling the SSH key checking altogether by running the following command in the terminal:

```
git config --global core.sshCommand "ssh -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null"
```

This will disable the SSH key checking and should allow you to clone or pull without freezing.

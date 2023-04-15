---
title: What would happen if two blobs had the same sha-1 hash value in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git would treat the two blobs as separate objects, even if they had the same SHA-1 hash.
---

**Contents**

[TOC]

### Git's Response

Git would not be able to handle a SHA-1 collision on a blob as it relies on the SHA-1 for identification and verification. If a SHA-1 collision occurred, the blob would be identified as two different objects, making it impossible for Git to determine which one is the correct version.

### Alternatives to SHA-1

Git could switch to an alternative hashing algorithm, such as SHA-256 or SHA-512, which are more secure and less likely to experience a collision. This would allow Git to continue to use the same type of identification and verification, while making it much more difficult for a collision to occur.

### Preventing SHA-1 Collisions

It is also possible to prevent SHA-1 collisions by using a stronger hashing algorithm and/or by using a longer hash. This would make it much more difficult for a collision to occur and would provide more security for the blobs stored in Git.

### Conclusion

Git would not be able to handle a SHA-1 collision on a blob, but it is possible to prevent such collisions by using a stronger hashing algorithm and/or a longer hash. This would provide more security for the blobs stored in Git and would make it much more difficult for a collision to occur.

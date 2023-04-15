---
title: Git is substituting line feeds (lf) with carriage return line feeds (crlf)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Git replaces LF with CRLF when core.autocrlf is set to true.
---

**Contents**

[TOC]

### What is LF and CRLF?
LF stands for Line Feed and is a special character (ASCII code 10) used to indicate the end of a line of text. CRLF stands for Carriage Return Line Feed and is a special sequence of two characters (ASCII codes 13 and 10) used to indicate the end of a line of text.

### Why is Git replacing LF with CRLF?
Git is designed to handle text files that use different line endings on different platforms. By default, Git will replace LF with CRLF when checking out text files from the repository, and will replace CRLF with LF when committing them. This ensures that the files are properly formatted for the platform on which they are being used.

### How to prevent Git from replacing LF with CRLF?
Git can be configured to prevent it from replacing LF with CRLF. This can be done by setting the core.autocrlf configuration option to false. This option tells Git to not automatically convert line endings and to leave them as is.

### What are the consequences of not replacing LF with CRLF?
If LF is not replaced with CRLF, the text files may not be properly formatted for the platform on which they are being used. This can cause the files to be displayed incorrectly or to not be recognized by the system. Additionally, it may cause issues when the files are edited, as the line endings may not be recognized.

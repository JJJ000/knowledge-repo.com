---
title: What is the purpose of the '# noqa' notation in Python comments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: # noqa is a comment tag used to ignore a line of code from being linted.
---

**Contents**

[TOC]

# What is '# noqa'?

'# noqa' is a comment tag used in Python code to indicate to a linter that a particular line should be ignored. A linter is a tool that checks code for potential errors and issues.

# How is '# noqa' Used?

'# noqa' is used to indicate to a linter that a particular line of code should be ignored. This is useful when the linter flags a line of code that is not actually an error, or when the code is written in a way that the linter does not understand.

# When Should '# noqa' Be Used?

'# noqa' should only be used when absolutely necessary, as it can be a sign of sloppy or incorrect code. It should also be used with caution, as it can mask underlying issues.

# What Are the Alternatives to '# noqa'?

The best alternative to '# noqa' is to refactor the code so that it is compliant with the linter and does not require any additional tags. This can often be achieved by making small changes to the code or by using a different coding style.

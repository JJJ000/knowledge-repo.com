---
title: Do I need to include a 'shebang' in my Python scripts, and what should it look like?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Yes, you should put a #! (shebang) in Python scripts, and it should take the form of #!/usr/bin/env python.
---

**Contents**

[TOC]

# Introduction

The #! (shebang) is a special syntax used in Unix-based operating systems that allows scripts to be run directly from the command line. It is typically used in scripts written in scripting languages such as Bash, Python, and Perl.

# Should I Put #! in Python Scripts

The answer to this question is generally yes, as it makes it easier to execute the script from the command line. However, it is not always necessary and it may not be necessary in all cases.

# What Form Should It Take

The form of the shebang should depend on the version of Python used. For Python 2.x, the shebang should be `#!/usr/bin/env python`, and for Python 3.x, the shebang should be `#!/usr/bin/env python3`.

# Conclusion

In conclusion, it is generally recommended to include a shebang in Python scripts to make it easier to execute the script from the command line. The form of the shebang should depend on the version of Python used.

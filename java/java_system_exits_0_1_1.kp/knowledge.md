---
title: The difference between system.exit(0), system.exit(-1), and system.exit(1) in Java is that exit(0) indicates that the program has completed successfully, exit(-1) indicates that the program has encountered an error, and exit(1) indicates that the program has been terminated by the user
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: System.exit(0) exits the program normally, System.exit(-1) exits with an abnormal termination status, and System.exit(1) exits with an error status.
---

**Contents**

[TOC]

### System.exit(0)
System.exit(0) is used to indicate that the program has completed successfully. It is the standard way of indicating that the program has terminated normally.

### System.exit(-1)
System.exit(-1) is used to indicate that the program has encountered an error and has terminated abnormally.

### System.exit(1)
System.exit(1) is used to indicate that the program has encountered a fatal error and has terminated abnormally.

### Summary
In summary, System.exit(0) is used to indicate that the program has completed successfully, System.exit(-1) is used to indicate that the program has encountered an error and has terminated abnormally, and System.exit(1) is used to indicate that the program has encountered a fatal error and has terminated abnormally.

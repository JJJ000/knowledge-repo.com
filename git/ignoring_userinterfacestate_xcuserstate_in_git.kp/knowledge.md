---
title: It is not possible to disregard userinterfacestate.xcuserstate
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git cannot ignore the UserInterfaceState.xcuserstate file as it contains important user-specific data.
---

**Contents**

[TOC]

### What is UserInterfaceState.xcuserstate?
UserInterfaceState.xcuserstate is a file created by Xcode, the integrated development environment (IDE) used to create apps for Apple's iOS and macOS platforms. This file stores the user interface state of the Xcode project, such as the position of windows, the size of the main window, and the active tabs in the project.

### Why is it important to include UserInterfaceState.xcuserstate in version control?
UserInterfaceState.xcuserstate is important to include in version control because it helps maintain consistency in the development environment. By version controlling this file, developers can ensure that the same settings are applied to the project regardless of who is working on it. This helps to reduce confusion and ensure that the project is built correctly.

### How to include UserInterfaceState.xcuserstate in Git?
Including UserInterfaceState.xcuserstate in Git is a simple process. First, add the file to the project's root directory. Then, add the file to the version control system by running the following command:

```git
git add UserInterfaceState.xcuserstate
```

Finally, commit the changes to the repository by running the following command:

```git
git commit -m "Added UserInterfaceState.xcuserstate"
```

### Conclusion
Including UserInterfaceState.xcuserstate in version control is important to ensure consistency in the development environment. The process of adding the file to Git is simple and straightforward. By following the steps outlined above, developers can easily ensure that their project is version controlled and that the user interface settings are maintained.

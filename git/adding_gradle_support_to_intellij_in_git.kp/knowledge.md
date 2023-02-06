---
title: How to enable gradle support in an intellij project
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The best way to add Gradle support to an IntelliJ project in Git is to import the project as a Gradle project from the IntelliJ welcome screen.
---

**Contents**

[TOC]

# Section 1: Create a Gradle Build File

The first step to add Gradle support to an IntelliJ project in Git is to create a Gradle build file. This build file will define the project structure, dependencies, and tasks that can be run through Gradle. The build file should be named `build.gradle` and should be placed in the root directory of the project.

# Section 2: Configure IntelliJ to Use Gradle

Once the Gradle build file has been created, the next step is to configure IntelliJ to use Gradle. This can be done by opening the IntelliJ project and selecting File > Settings > Build, Execution, Deployment > Build Tools > Gradle. Here, the user can select the Gradle version they want to use and also configure the project to use Gradle as the build tool.

# Section 3: Add Gradle Tasks to IntelliJ

The next step is to add Gradle tasks to IntelliJ. This can be done by selecting the Gradle tab in the IntelliJ project window and then selecting the “+” icon. This will open a window where the user can select the tasks they want to add from the build file. Once the tasks have been selected, they can be run from the Gradle tab in IntelliJ.

# Section 4: Commit Changes to Git

The final step is to commit the changes to Git. This can be done by selecting the VCS > Commit Changes option in IntelliJ. Here, the user can select the files they want to commit and also add a commit message. Once the changes have been committed, they will be available in the Git repository.

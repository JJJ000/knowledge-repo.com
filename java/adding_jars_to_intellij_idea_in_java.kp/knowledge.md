---
title: How to correctly include external jar files (lib/*.jar) in an intellij idea project
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Right-click on the project folder, select `Add Framework Support...`, then select `Global Library` and add the external JARs.
---

**Contents**

[TOC]

### Section 1 - Add Jars to the Project
1. Select the **File** menu, then select **Project Structure**.
2. In the **Project Structure** window, select **Modules** on the left side.
3. Select the **Dependencies** tab.
4. Click the **+** icon, then select **JARs or directories**.
5. Select the jar files from the lib directory, then click **OK**.

### Section 2 - Configure the Compiler
1. Select the **File** menu, then select **Project Structure**.
2. In the **Project Structure** window, select **Modules** on the left side.
3. Select the **Compiler** tab.
4. Select **Add** from the **Classpath** section.
5. Select the jar files from the lib directory, then click **OK**.

### Section 3 - Configure the Run Configuration
1. Select the **Run** menu, then select **Edit Configurations**.
2. Select the configuration you want to add the jars to.
3. Select the **Dependencies** tab.
4. Click the **+** icon, then select **JARs or directories**.
5. Select the jar files from the lib directory, then click **OK**.

### Section 4 - Build the Project
1. Select the **Build** menu, then select **Rebuild Project**.
2. The project will be built with the external jar files included.

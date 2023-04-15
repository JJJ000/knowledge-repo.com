---
title: How can I generate a .jar file or export a jar in intellij idea (similar to the eclipse Java archive export)?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In IntelliJ IDEA, you can create a .jar file by going to File > Project Structure > Artifacts, then selecting the desired files and clicking the `Build` button.
---

**Contents**

[TOC]

### Preparing the Project
1. Open the project in IntelliJ IDEA that you want to export as a JAR file.
2. Make sure that the project is compiled and all the necessary libraries are included.

### Exporting the JAR File
1. Select **File** > **Project Structure**.
2. Select **Artifacts** from the left side menu.
3. Click the **+** sign and select **JAR** > **From modules with dependencies**.
4. Select the main class of your project.
5. Click **OK**.

### Creating the JAR File
1. Select **Build** > **Build Artifacts**.
2. Select the artifact that you just created and click **Build**.
3. The JAR file will be created in the **out/artifacts** folder of your project.

### Running the JAR File
1. Open the command prompt.
2. Navigate to the directory containing the JAR file.
3. Type the command `java -jar <name_of_jar_file>.jar` and press Enter.
4. The application will start running.

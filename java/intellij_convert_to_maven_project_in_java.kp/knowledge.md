---
title: Change a Java project/module to a Maven project/module using intellij
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In IntelliJ, you can convert a Java project/module into a Maven project/module by right-clicking the project/module and selecting `Add Framework Support` and then selecting `Maven`.
---

**Contents**

[TOC]

### Prerequisites

Before converting a Java project/module into a Maven project/module, there are a few prerequisites that must be met:

1. The project must already be a Java project in IntelliJ.
2. The project must have a valid pom.xml file.
3. The project must be properly configured in the IntelliJ project settings.

### Convert to Maven

Once the prerequisites are met, the project can be converted to a Maven project/module. To do this, open the project in IntelliJ and go to `File > Project Structure`. Then, select the `Modules` tab and select the project you wish to convert. In the right panel, select the `Maven` tab and click on the `Enable Auto-Import` checkbox. This will enable Maven to automatically import any changes made to the pom.xml file. 

### Configure Dependencies

Once the project is converted to a Maven project/module, the next step is to configure the dependencies. To do this, open the pom.xml file and add any dependencies that are needed for the project. This can be done by adding the appropriate XML tags to the pom.xml file.

### Build the Project

Once the dependencies are configured, the project can be built. To do this, open the project in IntelliJ and go to `Build > Build Project`. This will compile and build the project, creating the necessary files and folders.

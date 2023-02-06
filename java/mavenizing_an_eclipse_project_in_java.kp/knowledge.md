---
title: Change an existing eclipse project to use maven
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Right-click on the project in the Eclipse Package Explorer and select `Configure > Convert to Maven Project`.
---

**Contents**

[TOC]

# Section 1: Prerequisites

Before beginning the process of converting an existing Eclipse project to a Maven project, there are a few prerequisites that should be met. 

1. Ensure that the Eclipse project is a valid Java project.
2. Install Maven Integration for Eclipse (m2e) plugin.
3. Install Maven in the local environment.

# Section 2: Configure Maven Project

Once the prerequisites have been met, the next step is to configure the Maven project. This is done by right-clicking on the project and selecting the "Configure" option. From the "Configure" menu, select "Convert to Maven Project". This will open the "New Maven Project" window.

# Section 3: Add Dependencies

The next step is to add any necessary dependencies. This is done by adding the appropriate Maven dependencies to the project's pom.xml file. This can be done manually or by using the Eclipse Marketplace.

# Section 4: Build the Project

Finally, the project can be built by running the Maven build command. This will compile the project and generate the necessary artifacts. Once the build is successful, the project can be deployed to a Maven repository.

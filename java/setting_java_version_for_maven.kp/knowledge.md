---
title: What is the process for configuring Maven to use a specific version of java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Set the desired Java version in the <project> element of the pom.xml file.
---

**Contents**

[TOC]

# Section 1: Installing Java
1. Download the desired version of Java from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Install the Java JDK by following the instructions provided on the website. 

# Section 2: Setting the JAVA_HOME Variable
1. Set the JAVA_HOME environment variable to the directory where the JDK was installed. 
2. This can be done by editing the system environment variable.
3. On Windows, this can be done by going to Control Panel > System > Advanced System Settings > Environment Variables.
4. On Linux, this can be done by editing the .bashrc file in the home directory.

# Section 3: Setting the Maven Java Version
1. Open the Maven settings.xml file, which is located in the .m2 directory in the user's home directory.
2. Add the following code to the settings.xml file to set the desired Java version:
    ```xml
    <profiles>
        <profile>
            <id>setJavaVersion</id>
            <activation>
                <activeByDefault>true</activeByDefault>
            </activation>
            <properties>
                <maven.compiler.source>1.8</maven.compiler.source>
                <maven.compiler.target>1.8</maven.compiler.target>
            </properties>
        </profile>
    </profiles>
    ```
3. Replace the 1.8 values with the desired Java version.

# Section 4: Verifying the Java Version
1. Run the following command to verify the Java version:
    ```
    mvn -version
    ```
2. The output should include the desired Java version.

---
title: Obtaining the Jackson jar from codehaus.org
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Download the Jackson jar file from the codehaus.org website.
---

**Contents**

[TOC]

# Downloading Jackson Jar

## Prerequisites
Before downloading the Jackson Jar, you will need to install the Java Development Kit (JDK) and the Apache Maven build tool.

## Downloading
1. Go to the [Jackson Codehaus page](http://jackson.codehaus.org/).
2. Click on the "Download" link on the right side of the page.
3. Select the version of the Jackson Jar you wish to download.
4. Click the "Download" button to begin the download.

## Installing
1. Open a terminal window and navigate to the directory where the Jackson Jar has been downloaded.
2. Execute the following command to install the Jackson Jar:
`mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging>`
3. Verify that the installation was successful by running the command `mvn dependency:list`. The Jackson Jar should be listed in the output.

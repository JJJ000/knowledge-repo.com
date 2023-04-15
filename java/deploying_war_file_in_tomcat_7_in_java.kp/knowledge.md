---
title: What is the process for deploying a war file in tomcat 7?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Deploy a war file in Tomcat 7 by copying the war file to the webapps directory of the Tomcat installation.
---

**Contents**

[TOC]

### Prerequisites 
Before deploying a war file in Tomcat 7, there are a few prerequisites to be aware of: 
- Tomcat 7 must be installed and running. 
- The war file must be compatible with the version of Tomcat 7 being used. 
- The war file must be placed in the webapps directory of the Tomcat installation. 

### Deploying the War File 
Once the prerequisites have been met, the war file can be deployed in Tomcat 7. To do this, follow these steps: 
1. Open the Tomcat 7 installation directory in your file browser. 
2. Copy the war file to the webapps directory. 
3. Open the Tomcat 7 bin directory. 
4. Execute the startup.bat file to start Tomcat. 

### Testing the Deployment 
Once the war file is deployed, it can be tested to ensure it is working properly. To do this, open a web browser and enter the following URL: 
http://localhost:8080/<war_file_name> 

If the war file was deployed successfully, the application should be visible in the browser. 

### Cleaning Up 
Once the war file has been tested and is working properly, it is a good idea to clean up the Tomcat 7 installation. To do this, open the Tomcat 7 bin directory and execute the shutdown.bat file. This will stop the Tomcat server and remove any temporary files that were created during the deployment process.

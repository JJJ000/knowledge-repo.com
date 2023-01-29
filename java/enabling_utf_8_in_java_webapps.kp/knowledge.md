---
title: What steps are needed to enable utf-8 encoding in Java web applications?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Ensure the web application is configured to use the UTF-8 character encoding.
---

**Contents**

[TOC]

1. **Configure the Web Server**

The first step is to configure the web server (e.g. Tomcat) to use UTF-8 as the default character encoding. This can be done by setting the URIEncoding attribute in the Connector element of the server.xml configuration file.

2. **Configure the Web Application**

The next step is to configure the web application to use UTF-8 encoding. This can be done by setting the pageEncoding attribute in the page directive in the JSP file, or by setting the charset attribute in the meta element in the HTML file.

3. **Configure the Database**

The third step is to configure the database to use UTF-8 encoding. This can be done by setting the character set of the database to UTF-8.

4. **Configure the JDBC Driver**

The last step is to configure the JDBC driver to use UTF-8 encoding. This can be done by setting the characterEncoding property in the connection URL.

---
title: An attempt to use 'system.web.helpers.json..cctor()' to access 'system.web.helpers.json.createserializer()' was unsuccessful
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The static constructor of System.Web.Helpers.Json is not allowed to access the method System.Web.Helpers.Json.CreateSerializer().
---

**Contents**

[TOC]

# Introduction
The error "Attempt by method 'System.Web.Helpers.Json..cctor()' to access method 'System.Web.Helpers.Json.CreateSerializer()' failed" occurs when trying to access a method that is not available in the System.Web.Helpers.Json namespace. This error is usually caused by a missing or incorrect reference to the System.Web.Helpers.Json namespace in the project.

# Symptoms
The most common symptom of this error is that the application will fail to compile when trying to access a method in the System.Web.Helpers.Json namespace. The error message will usually include a reference to the System.Web.Helpers.Json..cctor() method and the System.Web.Helpers.Json.CreateSerializer() method.

# Cause
The cause of this error is usually a missing or incorrect reference to the System.Web.Helpers.Json namespace in the project. This can happen if the namespace is not included in the project's references or if the reference is incorrect.

# Solution
The solution to this error is to add the correct reference to the System.Web.Helpers.Json namespace in the project. This can be done by right-clicking on the References folder in the Solution Explorer and selecting "Add Reference". Then, select the System.Web.Helpers.Json namespace and click "OK" to add the reference. Once the reference is added, the application should compile correctly.

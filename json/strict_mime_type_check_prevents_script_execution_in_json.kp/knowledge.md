---
title: Script execution was denied due to the enforcement of strict mime type checking
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The script cannot be executed because the MIME type is not supported.
---

**Contents**

[TOC]

# Introduction

The "Refused to execute script, strict MIME type checking is enabled" error occurs when a web browser refuses to execute a script due to a mismatch in the MIME type of the script and the content type of the response. The error is typically encountered when a web page attempts to load a script from a server with an incorrect MIME type.

# Causes

The "Refused to execute script, strict MIME type checking is enabled" error is caused by a mismatch between the MIME type of the script and the content type of the response. The MIME type of the script must match the content type of the response for the script to be executed. If the MIME type does not match, the browser will refuse to execute the script and display the error.

# Solutions

The solution to this error is to ensure that the MIME type of the script matches the content type of the response. This can be done by setting the correct MIME type in the response header. For example, if the script is a JavaScript file, the MIME type should be set to "text/javascript". Additionally, the server may need to be configured to serve the correct MIME type for the script.

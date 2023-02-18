---
title: How to turn on gzip compression for dynamic content on windows azure
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Enable dynamic compression for JSON content in IIS on the Windows Azure server.
---

**Contents**

[TOC]

## Section 1: Install URL Rewrite Module

The URL Rewrite Module is an extension for IIS 7 and above that enables the web server to perform URL rewriting. It can be used to enable Gzip HTTP compression on Windows Azure dynamic content in Json. To install, open the Server Manager, select the Roles node, and then select Web Server (IIS). Select Add Role Services from the Tasks menu. Select the checkbox next to URL Rewrite and then click Install.

## Section 2: Configure URL Rewrite Module

Once the URL Rewrite Module is installed, open IIS Manager, select the server node, and then select URL Rewrite. Click the Add Rules option in the Actions pane. Select the Blank Rule template, enter a name for the rule, and then click OK.

## Section 3: Configure Gzip Compression

To configure Gzip compression, open the URL Rewrite Module and select the rule you just created. Under the Conditions tab, click the Add button. Select {HTTP_ACCEPT_ENCODING} from the Condition input dropdown, enter gzip in the Pattern input, and then click OK.

## Section 4: Enable Gzip Compression

To enable Gzip compression, select the Actions tab. Select Add from the Action group dropdown, select Rewrite from the Action type dropdown, and then enter the following in the Action properties: 

`{HTTP_ACCEPT_ENCODING}` = `gzip`
`{RESPONSE_CONTENT_ENCODING}` = `gzip`

Click Apply in the Actions pane to save the changes. Gzip compression is now enabled for Windows Azure dynamic content in Json.

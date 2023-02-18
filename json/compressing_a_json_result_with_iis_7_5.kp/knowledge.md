---
title: What is the best way to reduce the size of a JSON response from an ASP.NET mvc application running on iis 7.5?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: You can compress a Json result from ASP.NET MVC with IIS 7.5 by enabling dynamic compression in IIS.
---

**Contents**

[TOC]

## Section 1: Install URL Rewrite Module

The URL Rewrite Module for IIS 7.5 is a free download from Microsoft. This module enables you to rewrite URL's on the server and to apply compression to the response. To install the URL Rewrite Module, download the module from the Microsoft website and install it on your server.

## Section 2: Configure URL Rewrite Rules

Once the URL Rewrite Module is installed, you can configure the rules to compress the response from the ASP.NET MVC application. To do this, open IIS Manager and select the website for which you want to enable compression. Then, select the URL Rewrite icon. Click on the “Add Rule(s)” button and select the “Blank rule” option.

In the “Name” field, enter a name for the rule, such as “CompressJsonResponse”. In the “Pattern” field, enter “(.*)\.json”. This will match all requests ending in “.json”. In the “Action” field, select “Rewrite” and in the “Rewrite URL” field, enter “{R:1}.json”. This will ensure that the request is rewritten to the original URL.

Next, click on the “Server Variables” button and add a new variable named “RESPONSE_Content-Encoding” with a value of “gzip”. This will ensure that the response is compressed using gzip compression.

## Section 3: Enable Dynamic Compression

To enable dynamic compression for the response, open IIS Manager and select the website for which you want to enable compression. Then, select the “Compression” icon. Check the “Enable dynamic content compression” checkbox and click on the “Apply” button.

## Section 4: Test the Compression

To test the compression, open a web browser and navigate to the URL of the application. The response should be compressed using gzip compression. You can use a tool such as Fiddler to verify that the response is compressed.

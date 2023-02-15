---
title: Rearranging the words 'chrome extension manifest matches' would give 'matches manifest extension chrome'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The `matches` field in a Chrome Extension Manifest is an array of URLs that determines which pages the extension will run on.
---

**Contents**

[TOC]

**Section 1: What is a Chrome Extension Manifest?**
A Chrome Extension Manifest is a JSON-formatted file that provides important information about a Chrome extension. This file is used by the Chrome Web Store to identify the extension, provide details about it, and list the permissions it requires. 

**Section 2: What are Manifest Matches?**
Manifest matches are a set of rules that specify which URLs an extension can access. They are defined in the manifest.json file and allow the extension to interact with certain web pages or websites.

**Section 3: What is the Syntax for Manifest Matches?**
The syntax for manifest matches is a set of key-value pairs. The key is the URL pattern, and the value is the type of access the extension requires. The types of access include "all_urls" for unrestricted access, "http://*/*" for access to all http sites, and "https://*/*" for access to all https sites.

**Section 4: What are the Benefits of Using Manifest Matches?**
Using manifest matches allows developers to control which websites an extension can access, which helps to ensure that the extension only interacts with the sites it is intended to. This helps to protect users from malicious extensions, as well as to ensure that the extension only accesses data that it is allowed to.

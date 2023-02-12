---
title: What are the security implications of using jsonp?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, JSONP is a safe and reliable way to make cross-origin requests for JSON data.
---

**Contents**

[TOC]

#### Security

JSONP is not secure, as it allows attackers to inject malicious scripts into the page, which can be used to hijack user sessions, deface websites, or redirect users to malicious sites. It also allows attackers to bypass the same-origin policy, which prevents websites from accessing data from other domains.

#### Cross-Origin Resource Sharing (CORS)

JSONP does not support Cross-Origin Resource Sharing (CORS), which is a mechanism that allows web applications to make requests to other domains. This means that JSONP requests are limited to the same domain, which can limit its usefulness.

#### Performance

JSONP is not as efficient as JSON, as it requires an additional script tag to be added to the page. This can increase page load times, as the script must be downloaded and parsed before the data can be accessed.

#### Usability

JSONP is easier to use than JSON, as it does not require any additional libraries or frameworks to be installed. It also makes it easier for developers to access data from other domains, as they do not need to worry about the same-origin policy.

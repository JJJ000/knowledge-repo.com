---
title: What is the process for retrieving a user's email address using the facebook graph api?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: It is not possible to get a user`s email from the Facebook Graph API in JSON format.
---

**Contents**

[TOC]

# Section 1: Overview

Facebook Graph API is an application programming interface (API) designed to allow users to access and manipulate data on the social media platform, Facebook. It provides a way for developers to use Facebook's data in their own applications and websites.

# Section 2: Accessing User Email

The Facebook Graph API allows developers to access user information, including their email address. To do this, the developer must first obtain a user access token from the user, which grants them access to the user's data. Once the token is obtained, the developer can make a request to the Graph API for the user's email address.

# Section 3: Retrieving Data in JSON

The Graph API can return data in several formats, including JSON. To retrieve the user's email address in JSON, the developer must make a GET request to the Graph API endpoint, passing in the user access token as a parameter. The response will be a JSON object containing the user's email address.

# Section 4: Example

For example, the following request will return the user's email address in JSON:

GET https://graph.facebook.com/me?fields=email&access_token=<USER_ACCESS_TOKEN>

The response will be a JSON object containing the user's email address:

{
  "email": "example@example.com"
}

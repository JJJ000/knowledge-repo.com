---
title: Making changes to existing data with the spring mvc patch method partial updates
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Yes, Spring MVC supports PATCH method for partial updates in JSON format.
---

**Contents**

[TOC]

# Overview
The Spring MVC PATCH method is an HTTP verb used to perform partial updates in a JSON request body. It is used to modify a resource without replacing it entirely. This method is used when a client wants to update only a specific part of a resource.

# Usage
The PATCH method is used to make a partial update to a resource. It is often used when the client only needs to update a few fields in the resource. The request body contains only the fields that need to be updated, and the server applies the update to the resource.

# Benefits
Using the PATCH method allows for efficient updates to a resource. The client only needs to send the fields that need to be updated, and the server will apply the update to the resource. This reduces the amount of data that needs to be sent over the network, and reduces the amount of work the server needs to do to apply the update.

# Limitations
The PATCH method is not suitable for all types of updates. If the client needs to update the entire resource, then the PUT method should be used instead. Additionally, the PATCH method is not supported by all web servers, and may not be available in all environments.

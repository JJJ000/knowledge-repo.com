---
title: The amazon aws command line interface is not accepting valid JSON in the payload parameter
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The AWS CLI requires that the payload parameter be a string, not valid JSON.
---

**Contents**

[TOC]

#Section 1: What is the Problem?
The problem is that Amazon AWS CLI is not allowing valid JSON in payload parameter in JSON.

#Section 2: What is AWS CLI?
AWS CLI is a command line interface that allows developers to interact with Amazon Web Services (AWS) from the command line. It is an open source tool that can be used to manage AWS services, such as EC2 instances, S3 buckets, and more.

#Section 3: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a language-independent format that is used to store and exchange data. JSON is used to structure data in a way that is easy for computers to read and manipulate.

#Section 4: Why is AWS CLI Not Allowing Valid JSON?
The problem is likely due to the way that the AWS CLI parses JSON. The AWS CLI attempts to parse the JSON payload as a single string, rather than as an object. This causes the AWS CLI to reject any valid JSON payloads as invalid.

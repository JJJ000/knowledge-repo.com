---
title: Strictmode Android blockguard policy error on network
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: StrictMode$AndroidBlockGuardPolicy.onNetwork throws an error if a network operation is detected on the main thread.
---

**Contents**

[TOC]

## Section 1: Overview
StrictMode$AndroidBlockGuardPolicy.onNetwork is a method in the Android StrictMode class that is used to enable or disable network access checks. It is used to control which network operations are allowed on the current thread.

## Section 2: How it Works
When enabled, StrictMode$AndroidBlockGuardPolicy.onNetwork will check for any network operations that are attempted on the current thread and throw an error if they are not allowed. This is done by checking the thread’s NetworkPolicy, which is set by the application at runtime. If the NetworkPolicy does not allow the attempted operation, an error will be thrown.

## Section 3: JSON
StrictMode$AndroidBlockGuardPolicy.onNetwork does not directly interact with JSON. However, if network operations are attempted on the current thread that include JSON, the method will check the NetworkPolicy to determine if the operation is allowed. If not, an error will be thrown. 

## Section 4: Conclusion
StrictMode$AndroidBlockGuardPolicy.onNetwork is a useful tool for controlling which network operations are allowed on the current thread. It is not directly related to JSON, but it can be used to prevent network operations that involve JSON from being executed.

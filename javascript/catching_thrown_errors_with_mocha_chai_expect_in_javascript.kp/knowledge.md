---
title: Expectations set up with mocha and chai are not capturing errors that are being thrown
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The expect.to.throw assertion must be used with a function that explicitly throws an error in order to catch it.
---

**Contents**

[TOC]

# Section 1: Overview
Mocha and Chai are two popular JavaScript testing frameworks that are used to test JavaScript code. Chai provides an expect.to.throw assertion that is used to test whether a given function throws an error. However, it is possible that the expect.to.throw assertion may not catch a thrown error in certain situations. 

# Section 2: Potential Causes
There are several potential causes for why the expect.to.throw assertion may not catch a thrown error. One potential cause is that the expect.to.throw assertion is not being used correctly. For example, if the expect.to.throw assertion is not correctly configured to expect a specific type of error, then it may not catch the thrown error. Another potential cause is that the error is being thrown asynchronously, which can cause the expect.to.throw assertion to miss the error.

# Section 3: Troubleshooting
If the expect.to.throw assertion is not catching a thrown error, then there are several steps that can be taken to troubleshoot the issue. The first step is to ensure that the expect.to.throw assertion is configured correctly to expect the correct type of error. If the expect.to.throw assertion is configured correctly, then the next step is to check if the error is being thrown asynchronously. If it is, then the expect.to.throw assertion may need to be wrapped in a setTimeout or Promise in order to catch the error. 

# Section 4: Conclusion
In conclusion, the expect.to.throw assertion in Mocha and Chai may not catch a thrown error in certain situations. If this occurs, then it is important to troubleshoot the issue to determine the cause. Potential causes include incorrect configuration of the expect.to.throw assertion and asynchronous errors. Troubleshooting the issue may involve ensuring that the expect.to.throw assertion is configured correctly and wrapping the expect.to.throw assertion in a setTimeout or Promise if necessary.

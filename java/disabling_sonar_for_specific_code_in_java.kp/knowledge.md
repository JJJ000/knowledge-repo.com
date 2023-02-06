---
title: Disabling sonar for specific code
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can turn off Sonar for certain code in Java by using the @SuppressWarnings annotation.
---

**Contents**

[TOC]

1. **Identify SonarQube Rules**

To turn off SonarQube rules for certain code in Java, the first step is to identify the rules that need to be disabled. This can be done by navigating to the Quality Profiles page in the SonarQube dashboard and selecting the profile that applies to the code being analyzed. From here, the user can view all of the rules associated with the profile and select the ones that need to be turned off.

2. **Disable Rules**

Once the rules that need to be disabled have been identified, the user can then disable them by going to the Quality Profiles page and selecting the “Deactivate” option for the desired rules. This will prevent SonarQube from running the rules on the code being analyzed.

3. **Add Comment**

To ensure that the code is still readable, it is important to add a comment to the code stating that the rule has been disabled. This will make it easier to identify which rules have been disabled and why.

4. **Re-Run Analysis**

Finally, the user should re-run the analysis to ensure that the rules have been successfully disabled and that the code is being analyzed correctly. This will help to ensure that SonarQube is not reporting any false positives.

---
title: What steps do I need to take to configure intellij idea for Android development?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To set up IntelliJ IDEA for Android applications in Java, install the Android SDK and create a new project with the Android template.
---

**Contents**

[TOC]

# Section 1: Install Android SDK

1. Download and install the latest version of the [Android SDK](https://developer.android.com/studio).

2. Once the installation is complete, open the Android SDK Manager and install the latest version of the Android Platform Tools.

3. Create an Android Virtual Device (AVD) for the emulator.

# Section 2: Configure IntelliJ IDEA

1. Open IntelliJ IDEA and go to the Preferences window (on Mac OS X, select IntelliJ IDEA > Preferences).

2. Select the Plugins option and then click the Browse Repositories button.

3. Search for and install the Android Support plugin.

4. Go to the Project Structure window (on Mac OS X, select File > Project Structure).

5. Select the Platform Settings tab and then click the SDKs option.

6. Click the Add (+) button and select Android SDK.

7. Select the Android SDK location and then click OK.

# Section 3: Create a New Android Project

1. Select the Create New Project option from the IntelliJ IDEA welcome screen.

2. Select the Android option from the list of project types.

3. Select the target Android API version and then click Next.

4. Enter the application name and package name, and then click Finish.

# Section 4: Run the Project

1. Select the Run option from the IntelliJ IDEA main menu.

2. Select the Run 'app' option from the list of available configurations.

3. Select the Android Virtual Device (AVD) from the list of available devices.

4. Click the OK button to run the application.

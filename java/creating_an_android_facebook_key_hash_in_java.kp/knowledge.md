---
title: What is the process for generating an Android facebook key hash?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the keytool command with the -exportcert argument and the alias and keystore information for your keystore.
---

**Contents**

[TOC]

# Section 1: Download OpenSSL for Windows
1. Download the OpenSSL binary [here](https://indy.fulgan.com/SSL/)
2. Extract the content of the zip file
3. Copy the `bin` folder and paste it in `C:\OpenSSL-Win32`

# Section 2: Create Keystore
1. Open `cmd`
2. Navigate to the `java` bin folder
3. Create the keystore with the command `keytool -exportcert -alias androiddebugkey -keystore %HOMEPATH%\.android\debug.keystore | C:\OpenSSL-Win32\bin\openssl sha1 -binary | C:\OpenSSL-Win32\bin\openssl base64`
4. Enter the password `android` when prompted

# Section 3: Retrieve Key Hash
1. Copy the output from the command prompt
2. Paste it into a text editor
3. Copy the key hash

# Section 4: Add Key Hash to Facebook
1. Go to your Facebook App's dashboard
2. Navigate to the `Settings` tab
3. Select `Basic` from the left-hand menu
4. Scroll down to `Android`
5. Paste the key hash in the `Key Hashes` field
6. Click `Save Changes`

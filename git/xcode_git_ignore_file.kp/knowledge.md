---
title: Xcode project git ignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: A `.gitignore` file should be added to the root of the Xcode project directory to ignore files that should not be tracked by Git.
---

**Contents**

[TOC]

#1 Xcode Derived Data

The Xcode-generated derived data folder holds the build products and indexes for your project. To ensure that these folders don't get tracked by Git, add the following line to your .gitignore file:

```
#Xcode
###
#gitignore contributors: remember to update Global/Xcode.gitignore, Objective-C.gitignore & Swift.gitignore

#Xcode
###
#User-specific config
xcuserdata/

#xcshareddata/

#Playground support files
*.playground/

#DerivedData
DerivedData/

#IntelliJ
###
### Created by https://www.gitignore.io/api/intellij
### Edit at https://www.gitignore.io/?templates=intellij

*.iml
*.ipr
*.iws
.idea/
```

#2 Xcode Workspace Settings

Xcode stores workspace-related configuration data in the .xcworkspace/xcuserdata folder. To ensure that these files don't get tracked by Git, add the following line to your .gitignore file:

```
#Xcode
###
#gitignore contributors: remember to update Global/Xcode.gitignore, Objective-C.gitignore & Swift.gitignore

#Xcode
###
#User-specific config
xcuserdata/

#xcshareddata/

#Playground support files
*.playground/

#DerivedData
DerivedData/

#Xcode Workspace Settings
*.xcworkspace/
```

#3 Xcode Plug-ins

Xcode stores plug-in related configuration data in the .xcuserstate folder. To ensure that these files don't get tracked by Git, add the following line to your .gitignore file:

```
#Xcode
###
#gitignore contributors: remember to update Global/Xcode.gitignore, Objective-C.gitignore & Swift.gitignore

#Xcode
###
#User-specific config
xcuserdata/

#xcshareddata/

#Playground support files
*.playground/

#DerivedData
DerivedData/

#Xcode Plug-ins
*.xcuserstate/
```

#4 Xcode Project Files

Xcode stores project-related configuration data in the .xcodeproj folder. To ensure that these files don't get tracked by Git, add the following line to your .gitignore file:

```
#Xcode
###
#gitignore contributors: remember to update Global/Xcode.gitignore, Objective-C.gitignore & Swift.gitignore

#Xcode
###
#User-specific config
xcuserdata/

#xcshareddata/

#Playground support files
*.playground/

#DerivedData
DerivedData/

#Xcode Project Files
*.xcodeproj/
```

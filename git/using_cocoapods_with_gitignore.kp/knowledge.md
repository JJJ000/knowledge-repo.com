---
title: What files should be excluded from version control when using cocoapods?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: A line for each Pod, such as `Pods/` and `*.xcworkspace`, should be added to the .gitignore file.
---

**Contents**

[TOC]

### Xcode Files

```
### Xcode
###
### gitignore contributors: remember to update Global/Xcode.gitignore, Objective-C.gitignore & Swift.gitignore

### Build generated
build/
DerivedData/

### Various settings
*.pbxuser
!default.pbxuser
*.mode1v3
!default.mode1v3
*.mode2v3
!default.mode2v3
*.perspectivev3
!default.perspectivev3
xcuserdata/

### Other
*.moved-aside
*.xccheckout
*.xcscmblueprint

### Obj-C/Swift specific
*.hmap
*.ipa
*.dSYM.zip
*.dSYM

### Playgrounds
timeline.xctimeline
playground.xcworkspace

### CocoaPods
Pods/
```

### CocoaPods Files

```
### CocoaPods
###
### We recommend against adding the Pods directory to your .gitignore. However
### you should judge for yourself, the pros and cons are mentioned at:
### https://guides.cocoapods.org/using/using-cocoapods.html#should-i-check-the-pods-directory-into-source-control
###
### Pods/

### CocoaPods Generated
*.xcworkspace

### Swift Package Manager
###
### Add this line if you want to avoid checking in source code from Swift Package Manager dependencies.
### Packages/
```

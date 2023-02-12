---
title: Required packages with varying levels of minimum stability for the composer
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, Composer allows for the specification of different minimum-stabilities for packages in the `require` section of the composer.json file.
---

**Contents**

[TOC]

#### Section 1: Setting the Minimum Stability

In a `composer.json` file, the `minimum-stability` setting can be used to specify the minimum stability level of packages that should be installed. This setting can be set to one of the following values:

- `stable`
- `RC`
- `beta`
- `alpha`
- `dev`

#### Section 2: Setting Different Minimum Stabilities for Different Packages

It is possible to specify different minimum stabilities for different packages. This can be done by adding an extra `minimum-stability` key to the `require` section of the `composer.json` file. For example, the following code will install the `example/package-a` package with a minimum stability of `stable`, while the `example/package-b` package will require a minimum stability of `beta`:

```json
"require": {
    "example/package-a": "^1.0",
    "example/package-b": "^2.0",
    "minimum-stability": {
        "example/package-a": "stable",
        "example/package-b": "beta"
    }
}
```

#### Section 3: Setting a Global Minimum Stability

It is also possible to specify a global minimum stability level that will be used for all packages. This can be done by setting the `minimum-stability` key in the `config` section of the `composer.json` file. For example, the following code will set the minimum stability level to `beta` for all packages:

```json
"config": {
    "minimum-stability": "beta"
}
```

#### Section 4: Overriding a Global Minimum Stability

If a global minimum stability has been set, it is possible to override it for specific packages. This can be done by adding an extra `minimum-stability` key to the `require` section of the `composer.json` file. For example, the following code will install the `example/package-a` package with a minimum stability of `stable`, while all other packages will require a minimum stability of `beta`:

```json
"require": {
    "example/package-a": "^1.0",
    "minimum-stability": {
        "example/package-a": "stable"
    }
},
"config": {
    "minimum-stability": "beta"
}
```

---
title: What is the syntax for passing parameters to a controller using ui-sref in ui-router?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Pass parameters using ui-sref by adding them as an object to the state configuration in the $stateProvider.
---

**Contents**

[TOC]

# Section 1: Create the ui-sref Link

The first step is to create the ui-sref link in the HTML template. This is done by using the `ui-sref` directive. The syntax for the `ui-sref` directive is as follows: 

```html
<a ui-sref="stateName({param1: value1, param2: value2, ...})">Link Text</a>
```

The `stateName` is the name of the state that you want to transition to, and the `param1`, `param2`, etc. are the parameters that you want to pass to the controller. The values of these parameters are set in the `value1`, `value2`, etc. fields. 

# Section 2: Configure the State

The second step is to configure the state in the router. This is done by using the `$stateProvider` service in the application configuration. The syntax for the `$stateProvider` service is as follows: 

```javascript
$stateProvider.state('stateName', {
    url: '/url',
    templateUrl: 'template.html',
    controller: 'ControllerName',
    params: {
        param1: null, 
        param2: null,
        ...
    }
});
```

The `stateName` should match the name of the state specified in the `ui-sref` link, and the `param1`, `param2`, etc. should match the parameters that you want to pass to the controller. The `url` is the URL of the state, the `templateUrl` is the URL of the HTML template, and the `controller` is the name of the controller.

# Section 3: Access the Parameters in the Controller

The third step is to access the parameters in the controller. This is done by injecting the `$stateParams` service into the controller. The `$stateParams` service contains an object with all of the parameters that were passed in the `ui-sref` link. The syntax for accessing the parameters is as follows: 

```javascript
$stateParams.param1 // value1
$stateParams.param2 // value2
```

# Section 4: Use the Parameters

The fourth and final step is to use the parameters in the controller. This can be done by using the values of the parameters in the controller logic. For example, if the `param1` parameter was passed in with the value `value1`, then the controller could use this value to perform some logic. 

```javascript
if($stateParams.param1 === 'value1') {
    // Do something
}
```

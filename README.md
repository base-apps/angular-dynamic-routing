# Angular Dynamic Routing
An angular module designed to create [ui-router](https://github.com/angular-ui/ui-router) states dynamically via a state configuration object.  Use the optional animation module to provide fancy animations during state transitions.

These modules were originally part of [Foundation for Apps](https://github.com/zurb/foundation-apps) and later [Angular Base Apps](https://github.com/base-apps/angular-base-apps), but now exist in their own standalone project.

## Install

Get started by installing angular-dynamic-routing from npm.

```bash
npm install angular-dynamic-routing --save
```

This library is often combined with [base-apps-router](https://github.com/base-apps/base-apps-router) which can be used to create the state configuration objects.

## Usage

Include the dynamic routing modules and source code:
- `dynamicRouting` - node_modules/angular-dynamic-routing/dynamicRouting.js
- `dynamicRouting.animations` (optional) - node_modules/angular-dynamic-routing/dynamicRouting.animations.js

The `dynamicRouting` module can configure states in one of two ways:

1. Assign the state configurations to a `BaseAppsRoutes` global variable
2. Pass the state configurations to the `$BaseAppsStateProvider.registerDynamicRoutes` method during the config phase of your application

## Modules

### dynamicRouting
**Dependencies**: ui.router

Uses the provided state configuration objects to create states for ui-router.

The module also includes a DefaultController which exposes the variables declared in the state configuration object.

### dynamicRouting.animations (optional)
**Dependencies**: ngAnimate, dynamicRouting

This module is an optional add-on which allows the dynamically routed views to animate as long as there is an animationIn and an animationOut in the state configuration object.

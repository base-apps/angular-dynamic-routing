# Angular Dynamic Routing
An angular module designed to create [ui-router](https://github.com/angular-ui/ui-router) states dynamically via a state configuration object.  Use the optional animation module to provide fancy animations during state transitions.

This module was original part of [Foundation for Apps](https://github.com/zurb/foundation-apps) and later [Angular Base Apps](https://github.com/base-apps/angular-base-apps) but now exists as a standalone project.

## Install

Get started by installing angular-dynamic-routing from npm.

```bash
npm install angular-dynamic-routing --save
```

This library is often combined with [angular-front-router](https://github.com/base-apps/angular-front-router) which can be used to create the state configuration objects.

## Usage

First include the `dynamicRouting` module, and optionally the `dynamicRouting.animations` module, in your angular app.

The `dynamicRouting` module can configure states in one of two ways:

1. Assign the state configurations to a `foundationRoutes` global variable
2. Pass the state configurations to the `$FoundationStateProvider.registerDynamicRoutes` method during the config phase of your application

## Modules

### dynamicRouting
**Dependencies**: ui.router

The dynamic router runs its own .config function when it's injected which digests out `foundationRoutes` object created by angular-front-router.

The module also includes a DefaultController which exposes the variables declared in the front-matter.

### dynamicRouting.animations
**Dependencies**: ngAnimate, foundation.dynamicRouting

This module is an optional add-on which allows the dynamically routed views to animate as long as there is an animationIn and an animationOut in the front-matter of the template

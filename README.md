[![Build Status](https://img.shields.io/travis/MaritzSTL/mtz-ajax-interceptor/master.svg?style=flat-square)](https://travis-ci.org/MaritzSTL/mtz-ajax-interceptor)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/owner/my-element)

# \<mtz-ajax-interceptor\>

A group of elements to support intercepting ajax requests for injecting headers, url rewriting or handling responses globally.

## Elements

### `<mtz-ajax-interceptor>`
An implementation of `mtz-ajax-interceptor-behavior` useful for quick implementations, ie. demos. This allows other interceptors to be slotted in.

### `<mtz-auth-interceptor>`
An implementation of the mtz.InterceptorBehavior that injects auth headers based on the event.target containing the [with-auth] attribute. 

### `<mtz-presend-header-interceptor>`
An implementation of the mtz.InterceptorBehavior that injects a header:value onto a presend event for iron-ajax.

### `<mtz-status-code-interceptor>`
An implementation of the mtz.InterceptorBehavior that compares a status property against the status code in the event to determine if the interceptor logic should run or not.

### `<mtz-url-rewrite-interceptor>`
An implementation of the mtz.InterceptorBehavior that rewrites matching requests request url to a new url onto a presend event for iron-ajax.

## Behaviors

### `mtz.AjaxInterceptor`
Handles registering declarative interceptors then listening for all registered events and calling the interceptors associated with those events.

### `mtz.Interceptor`
Used to create an instance of an interceptor that allows for declarative registration for binding logic to a bubbling event that is not a child of the element.


## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Viewing Your Element

```
$ polymer serve
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

# Microfrontends

## Status

Accepted

## Context

In the current system, whenever a change is made, it takes a long time, and introduces risk to breaking another part of the application.

## Decision

Decouple the frontend deployments by utilizing Microfrontends to allow us to deploy an individual component more frequently with less coupling on other parts of the system.

## Consequences

What becomes easier or more difficult to do because of this change?
* Smaller, more frequent releases will reduce risk on each release.
* Forces a strong separation between various parts of the system.
* Page load times should decrease because we are only loading the parts of the single page app necessary to render the current request.
* At first glance, it seems that deploying more of these microfrontends might be harder than the current monolith deployment, but from experience, once the deployment pattern is set up, we should see that it is actually simpler.



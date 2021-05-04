# Architecture Decision Records

# Serverless

## Status

Accepted

## Context

The current system is having scaling issues with the number of users.  The application has very low usage at night because the sysops squad only works between 9am-9pm in one time zone.  However, it does need to scale up slightly during the day in order to handle the traffic.

## Decision

The team discussed alternatives, like running a Kubernetes cluster, but we decided that since usage varies a lot between day and night, and the amount of users varies based on customer counts, we decided on using a Serverless architecture.  The team can implement this with either AWS Lambda or KNative.

## Consequences

* Autoscaling based on traffic gets easier
* The application will become highly available, and improve the user experience
* Site Reliability improves
* Managing security roles on lambda functions is more challenging, but improves the overall security posture of the applicaiton.

# Domain Breakdown

## Status

Accepted

## Context

In the current system, whenever a change is made, it takes a long time, and introduces risk to breaking another part of the application.

## Decision

Deploy discrete serverless functions for each domain.

## Consequences

What becomes easier or more difficult to do because of this change?
* Smaller, more frequent releases will reduce risk on each release.
* Clear boundaries between system components helps achieve seperate concerns, giving each independent function a well-defined purpose.
* Though we recognize that this is not internet scale, we see a need for individual components to scale independently.




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



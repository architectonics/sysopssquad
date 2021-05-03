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
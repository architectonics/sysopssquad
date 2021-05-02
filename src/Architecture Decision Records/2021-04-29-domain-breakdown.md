# Domain Breakdown

## Status

Proposed

## Context

In the current system, whenever a change is made, it takes a long time, and introduces risk to breaking another part of the application.

## Decision

Deploy discrete serverless functions for each domain.

## Consequences

What becomes easier or more difficult to do because of this change?
* Smaller, more frequent releases will reduce risk on each release.
* Clear boundaries between system components helps achieve seperate concerns, giving each independent function a well-defined purpose.
* Though we recognize that this is not internet scale, we see a need for individual components to scale independently.



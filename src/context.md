**Sysops Squad Architecture**
The Sysops Squad system has several types of users outlined above:
* Customer
* Manager
* Administrator
* Call Center
* Expert

We aim to design a system pleasing to each of their unique needs in the environment.  Some key architectural characteristics in our design include
* **Availability** - The users are currently reporting a lot of downtime, due to increased amount of users on the system.  To support this, our Arhitecture Decision Records (left navigation) documents why we chose Serverless and Microfrontends as key elements of our architecture.
* **Reliability** - Lost tickets or times when we send the wrong expert to help a customer not only cost the Sysops Squad revenue on those individual instances, but these instances also represent a substantial risk to our ongoing reputation.  According to [Reputation Refinery](https://reputationrefinery.com/96-of-unhappy-customers-wont-complain-to-you-but-will-tell-15-friends-infographic), 96% of customers won't complain to us, but will tell 15 friends about their bad experience.  To this end, we are building a robust Scheduling System.
* **Cost Optimization** - Though we recognize that we'll never have millions of users using our site at once, we did want an option that allows us to scale to zero.  In looking at our usage patterns, we observe that there are many hours of the day where we just don't have any users.  Our Lambda architecture allows for this.
* **Releasability** - Change is too hard in the current system.  When a developer changes something in one part of the app, it unexpectedly impacts other parst of the app.  We aim to address that by using the domain boundaries to develop individually deployable units -- either microfrontends or lambda functions as the APIs.  

**C4 Diagrams** 
Our team chose to try the [C4 Model](c4model.com) approach to diagrams.  This page has the context diagram, and the next diagrams are the container diagrams.  We expect to collaborate with the developers on the Component level diagrams as we get closer to implementation.

**Architecture as Code**
We decided to implement our diagrams as text files, enabling us to comment on individual lines in the pull requests and to collaborate better than if we were committing rendered images.

**Contributing** 
This is an active work in progress, and we'd encourage your input.  Please find the instructions on how to contribute [here](https://github.com/architectonics/sysopssquad/blob/main/contribute.md)..
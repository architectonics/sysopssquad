# Web Application

Per our Architecture Decision Records (navigation on the left), our team is recommending a serverless approach with microfrontends.  Together, this allows the engineering team to release any individual component once it is tested in as independent of a manner as possible.

While there are options, the architecture team has had some experience with SingleSPA.js as a root microfrontend that allows loading of different javascript modules based on the route of the current request.  We expect that this kind of technology will introduce some performance benefits for the users of the site.

Additionally, when a change needs to be made to the ticketing frontend, there's a targeted backend where serverside changes can be isolated.  We are recommending this be deployed using a Lamda architecture, which will help with independent deployments and can be an important part of the solution to the reliability issues that users have experienced in the current system as a result of increased user counts.
# Mobile Application

Once the ticket is assigned to an Expert by the Scheduling System, a text is sent out to the Expert regarding the ticket. The Expert can review the assigned ticket on the Mobile App.

The Mobile App is broken down into four modules: Single Signon, Expert Module, Ticketing Module, Knowledge Base Module. Single Signon allows the Expert to login and caches the token for future login with a specified expiry time. Expert Module captures expert availability and location. Ticketing Module communicates the status of the ticket and captures all comments. Knowledge Base Module provides searches on the articles from the history and also allows to add new articles.

All these modules interact with the API gateway to read/write the data via respective APIs
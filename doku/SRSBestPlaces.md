# Software Requirements Specification
## Introduction
### Purpose
This SRS will further define our Project and the requirements.
### Scope
BestPlaces will be a service, which allows you to store information about places you have visited and you may want to visit in the future. In the first place our application is useful on mobile, but also on Pc to plan trips. Therefore, we will focus on a mobile-first and responsive website, which will support all platforms.
### Definitions, Acronyms and Abbreviations
| Acronym | Description |
| ------- | ----------- |
| Vaadin | GUI-Framework based on Google Web Toolkit, which enables Java to make websites. |
| ODOD | On-Demand-Own-Data |
| RESTful API | Web-Service to gather data from a server. |
| MVC | Model-View-Controller. Division of data, processing and view. |
### Preferences
Not applicable
### Overview
BestPlaces is all about your favorite places. You can track where you were and it will tell you what you might like to visit.
The user should be able to add visited places by also providing additional information to the place. For example, if he wants to go there again or how expensive it was. By providing this information we’re able to give personalized recommendations for places the user might want to visit. Additionally, this data can be used to help other users to get information about the place.
## Overall Description
On the following page we provided our Overall User Case Diagram, which briefly depicts the features of out application and when there will be implemented.
![General Overall Use-Case-Diagram](GOUCD.png)
### Product perspective
BestPlaces will make it easier to track your favorite places. Our target is defined by total comfort for the user. Every function and any use should be as easy as it could. The user should have fun to use the application instead of get bored or angry about it. So our claim is it to build an application which is easily to use, appealing in style, multisided in use and never gets disliked by the user.
### Product Functions
The user should be able to track his favorite places as well as those, where he might want to go. A ‘Place’ includes information like GPS coordinates, costs, opening hours, own experience, the possibility to perceive which food the user wants to eat in the future and of course the option to get opinions about this place from other users. Furthermore, the user has the option to chart his places by for example the number of visits, the money he spent, the food he ate and so on.
### User Characteristics
Our application is suitable for everyone who likes to gather information about the own lifestyle. Due to the analysis of the tracked data one can find out more about the behavior of oneself.
### Constraints
Our project is only by time, effort and missing work equipment restricted. There are many good ideas for our application but in the given time it is not possible to implement all of them.
### Assumptions and dependencies
- IDE: IntelliJ and PyCharm
- Version control: GitHub
- Scrum: JIRA
- Programming language: Python, Java
- Database: MySQL
- Test: Junit,…

## Specific Requirements
### Functionality
#### User-Management
The user-management includes everything concerning the management of the users. These should be able to sign-up and log-in to the service and their data should be stored in the database. Therefore, it should be possible for the user to have exact data on all devices. [Use-Case Document for Sign-up](https://github.com/anonfreak/bestplaces/blob/master/doku/Sign%20Up/UCSSignUp.md) and [Use-case Document for Edit User Data](https://github.com/anonfreak/bestplaces/blob/master/doku/Edit%20User%20Data/UCSEditUserData.md)
#### Search
To make it easier for the user to find and track places without providing all information by themselves, there should be a small search engine for these places. Further information:
[Use-Case Document for Searching](https://github.com/anonfreak/bestplaces/blob/master/doku/searching/Use%20Case%20Specification%20Searching.pdf)
After searching for places the User can click at them to see more information about this place. This is described in detail in following document. [Use-case document GetInformation](https://github.com/anonfreak/bestplaces/blob/master/doku/ManageVisits/UCSManageVisits.md)
#### Timeline (Tracking Places)
The “Timeline” displays all places, the user visited and the user may plans to visit (with fixed date) in the future. It will be displayed after logging in. To track places, the user should have the ability to add and edit his places. [Use-case Document for View Timeline](https://github.com/anonfreak/bestplaces/blob/master/doku/ViewTimeline/UCSViewTimeline.md), [Use-case Document for Add Visit](https://github.com/anonfreak/bestplaces/blob/master/doku/AddVisit/AddVisit.md) and [Use-case Document for Manage Visits](https://github.com/anonfreak/bestplaces/blob/master/doku/ManageVisits/UCSManageVisits.md) 
#### Favorites
The user should be able to save their favorite places and places they may want to visit in the future, but without defining any date.
[Use-Case Document for Favorites](https://github.com/anonfreak/bestplaces/blob/master/doku/Favorites/Use%20Case%20Specification%20Manage%20Favorites.pdf)
#### Statistics
The application should present statistics about the places the user visited. This include costs, how often the place was visited and many more.
#### Interaction
To enable users to add their own places and provide additional information, we use our “ODOD”-Model (“On-Demand-Own-Data”), which means that if the user adds places or information about it, we will make a data record in our databases for that place which will further be used for that place.
#### Recommendations
Based on user data we may be able to give recommendations on places, the User might be interested in.
### Usability
#### User-Interface
The application will be easy to use, due to a clean and structured user-interface. To provide full usability on most possible devices, the web-client should be responsive.
### Reliability
#### Server Status
The server should always be running and online to provide full functionality. Therefore, it should be developed carefully and without minor bugs. Even if there is a bug, the server should be able to stay running and ignoring the bug.
#### Web-Client
The web-client should always be running, because it’s the main interface of the application. This will be accomplished by using exception-handling.
### Performance
#### Speed
Because of the server-client architecture we are able to provide high speed on client devices. The speed of our webclient is depending on the amount of users and general server load.
#### Capacity
Our server is running on a hosted Linux-Server located in Frankfurt. Because our financial resources are limited this server has a rather low speed in data processing and not that much disk space. Therefore, we aren’t able to handle thousands of people using our applications. Nevertheless, we could expand rather quickly by using a bigger Linux-server.
#### Response Time
Our Server is located in Frankfurt in a big data center with high-speed internet connection. Therefore, we should be able to provide quick response times concerning internet connection. Depending on the amount of users the response times could be worse, because it’s not a high-performance server.
### Supportability
#### Compatibility for server software
To develop out server, we will use python and MySQL, which nearly runs on every system. Therefore, we’re able to easily switch between systems.
The server has to handle different database types and switching between database management systems should be as easy as possible.
#### Clients
Our web-client is based on Vaadin, which uses JavaScript to display the website. Therefore, the web-client should run in every modern browser, which supports JavaScript. To provide full usability we will may implement a native Android-app.
### Design Constraints
#### Application architecture
Our application will be based on a server-client-structure. The Server will be responsible for data warehouse and data processing. To easily communicate with clients, we will provide a RESTful API, which enables interaction with the server on nearly every client.
#### MVC-Model
Our application should strictly follow the MVC-model to lower the effort for implementing new clients and to write clean and understandable code.
### On-line User Documentation and Help System Requirements
Not applicable.
### Purchased Components
Not applicable.
### Interfaces
#### User-Interfaces
On the web the Interface is written in Java using the Vaadin GUI-framework. As described before the main view should be a timeline, which presents the user places he visited and is planning to visit. Moreover, there should be a search bar on the top, which enables the user to search places.
#### Hardware Interfaces
No defined hardware.
#### Software Interfaces
To get as much information as possible about places, we will communicate with the Google Place API, which provides all information on places from Google. Additionally, we will reuse other API’s, like TripAdvisor to provide even more information.
#### Communications Interfaces
We will use a server-client-model, which divides data warehouse and data processing from the client, which the user will interact with. This makes it possible to support all kind of devices, because we do not need to implement our logic on every device. Moreover, it speeds up the client application.
The server, which the client has to interact with, will be based on Python which provides web services by a RESTful API. Information about the interfaces will follow.
### Licensing Requirements
Not applicable.
### Legal, Copyright and other notices
Not applicable.
### Applicable Standards
Not applicable.
## Supporting information

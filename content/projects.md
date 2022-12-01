+++
title= "Projects"
description = "Page developed in Hugo"
date = "2022-10-04"
author = "Shashank sarma"
+++

*P.S: The projects I have worked are explained in length here. Techincal terms and my role has been highlighted in case of quick reading.*

## HARMAN International  
(2021 - *till date*)  
Lead engineer  
**Client** : Microsoft
Project : Confidential  

This project was a tool used by the clients to monitor their project statuses. This was an end to end solution to the non technical share holder to understand the delivery, revenue, work status, expenditure and other aspects of a project they are handling. This tool would handle creation of a project, forecasting revenue and expenditure, blockers like 'Risks, Actions, Issues', report generation using 'PowerBI' etc., This was a monolith application with structure as big as 70-80 projects packed into one .net solution file. Our team's responsiblities were to identify the functionalities that can become micro services and design-develop-deploy them.

1. *Authentication platform*: The existing micro services were aunthentication and authorizing the user at their own level per each request. This was an operational overhead. So to overcome this we had to create an AuthZ platform which can do the job for these services uniquely. The authorization must happen based on various factors that were stored in database like role of the user, claims he has, confidentiality level of the particular project, timezones the project exist in. In case of UI, the authorization must happen against the resources i.e; pages, button, images, download/upload permissions and other UI elements/functionalities.  
This micro service would sit behind an **APIM** in a private network, any micro service/UI request that needs AuthZ will hit an incoming uri of the APIM and the service would return a token containing the suitable resources for the user to access or a custom message in case of no authorization.  
This micro service was built on **Azure Fucntions v4** and **.Net 6**, so that we have serverless functions run in an isolated environment. MS-SQL was used as the database. **Azure service bus** was used for messaging between micro services.  
My responsibilities were as belows;  
    1. **Work closely with the product owner(client) and architect to understand the requirements and HLD.**  
    2. **Sketch out LLDs and generate component level documentation, get it approved by the client.**  
    3. **Hand over work items to other team members, keep some to self.** 
    4. **Address the technical issues within the team.** 
    5. **Review and approve the PRs raised by peers.**
    6. **Work closely with the testing team to generate the test cases as rigid as possible.**
    7. **Work closely with DevOps team to get the application deployed rightly**  
---
2. *Azure DevOps Boards integration*: The application had to be integrated with Azure devops boards so that whenever any item is created on the project's Azure boards it gets synced into the application and viz. The items once synced had to become read only on the application and can only be edited via Azure board. The challenege here was one project can involve multiple vendors working with multiple azure boards. Consistency of the system shouldn't be effected when the syncing of items happen. This micro service also had to have a notification service to send emails periodically to responsible people about the item's due date or status change etc.  
This micro service was built on **Azure Fucntions v4** and **.Net 6**, so that we have serverless functions run in an isolated environment. MS-SQL was used as the database. **Azure service** bus was used for messaging between micro services. Azure devops boards had to use Webhooks to let the sync happen.  
    1. **Work closely with the product owner(client) and architect to understand the requirements and HLD.**  
    2. **Sketch out LLDs and generate component level documentation, get it approved by the client.**  
    3. **Hand over work items to other team members, keep some to self.** 
    4. **Address the technical issues within the team.** 
    5. **Review and approve the PRs raised by peers.**
    6. **Work closely with the testing team to generate the test cases as rigid as possible.**
    7. **Work closely with DevOps team to get the application deployed rightly**

**Client** : Pointsbet
Project : Winx  
PointsBet is a leading sports betting company based in [Australia](www.pointsbet.com.au) and [USA](www.il.pointsbet.com). They specialize in horse race bookmaking in Australia and venturing into USA horse races. They have partenered up with another company called [Xpressbet](www.xpressbet.com)  
My responsibilities were as belows;  
1. *Authorization server:*  
The application has to enable user of Pointsbet sportsbook to be on pointsbet horse races. To do this, Any exisiting/new user of pointsbet sportsbook or Xpressbet needs to register themselves with the applicaiton and get the applcable KYC done. To enable this, we had to use OAuth2.0 concept. We used [Duende Identity server](https://duendesoftware.com/products/identityserver) on top of an .Net Core 3.1 Web app. This will sit behind an APIM in a private network and exposes two endpoints to genrate a token and to autorize. The application should read user data and KYC status from a universal store hosted in **Azure Cosmos DB**
My responsibilities were as belows;  
    1. **Understand the requirements from the clients(USA & AU)**
    2. **Follow the HLDs and LLDs created by the client and develop the application**
    3. **Deploy the application using Docker images via CI/CD pipelines**  
2. *Global Pre-Registration:*  
The application has to let user pre-register themselves before the racing/sporting season begins to avail exclsuive special offers. This was an **Azure function V4** built on **.Net 6**. The application should read, write user data from/into a universal store hosted in **Azure Cosmos DB**
My responsibilities were as belows;  
    1. **Understand the requirements from the clients(USA & AU)**
    2. **Follow the HLDs and LLDs created by the client and develop the application**
    3. **Deploy the application using Docker images via CI/CD pipelines**  
---
## S&P Global  
(2019-2021)  
Senior Software Engineer  
Product development  

1. *Data Pipelines:*  
There were upstream databases from which data fragments flow into the decision making system. To combine these fragments into relative segments and make a meaningful content, we had to maintain data pipelines using **.net 4.8** and **OData API services**. The data fragments would be broadcasted on **Kafka** streams. We had to modernize some of these pipelines into **.net core 2.1**  
My responsibilities were as belows;  
    1. **Work with onsite teams in managing data pipelines (development and release).**
    2. **Extract data from Kafka services, normalize, validate and send it forward to various databases that serve the UI.**
    3. **Involves using Odata apis, C#, Kibana, Kafka, MS-SQL messaging queue.**

2. *CI/CD enablement:*
The above mentioned pipeline where deployed into physical servers manually after jenkin build pipeline stage. I was the point of contact in the team to migrate and automate the process to **Azure Devops build and release pipelines**  
My responsibilities were as belows;  
    1. **Migrated VSTS-Jenkins to Azure DevOps.**
    2. **Migrate code repositories to Azure DevOps, implement Continuous Integration, Deployment, Testing (CI-CD-CT).**
    3. **Automate and improve the release (to various environments) procedures.**

3. *Ratings 360 UI:*
The organization was developing a single UI solution for all the data representation of various customers. This was done by using **ReactJs**, **NodeJs**. We followed **Micro front end** architecture.  
My responsibilities were as belows;  
    1. **Work with the UK based product owner to understand the requirements**
    2. **Handle scrum activities like organizing daily stand up, retrospective, story grooming, scrum of scrums**
    3. **Implement the micro front end stubs given assigned using React**
---
 ## Rythmos Incorporation 
(2018-2019)  
**Client** : Ubisoft  
Consultant  
Project : DocWorks CMS  

Ubisoft is gaming gaint specializing in game development and publishing them across various platforms. The project dealt with creating an application that can generate documentation of the code base based on the documentation comments and meta data generated by **Roslyn compiler** and publish to it the internet. This project consisted of 7 micro-services followed a **Staged Event Driven Architecture (SEDA)**. All the micro services were **Azure web apps** and one was running on a **Azure Virtual Machine**. Project was built on **.Net core 2.1**. **Asp.Net WEB API** was used as face of the back end. **SignalR** was used to fetch real time notifications. We used **MongoDB** for data storage and **Kibana** as visualization and logging tool. **Angular 7** was used as the UI framework. **Xunit** and **Mongo2Go** were used to write unit test cases  
My responsibilities were as belows;  
    1. **Write unit test cases and achieve the desired coverage(75%). We could achieve 90% here.**  
    2. **Understand the requirements from team lead and work on the given modules.**  
    3. **Work closely with the testing team to get the modules tested.**  
    4. **Participate in daily scrum activities.**  
   
 ---  
## Altura Consulting  
(2017-2018)  
Product development
The company has their own framework written for SAP Business one tool. This was a HR tool for organizations. The framework was written in **.Net 3.5**. **SAP Hana** and **MS-SQL** were used for databases. **Crystal reports** was used to generate reports.  
My responsibilities were as belows;  
    1. **Address the change requests on the framework that are respective to clients**.  
    2. **Implement new features as described by the product owner**.

---
## HCL Technologies  
(2014-2017)  
**Client** : Microsoft  
Game offer is a website where gamers can invite friends to join the gaming console family.

# Test Plan
## 1.	Introduction
### 1.1	Purpose
The purpose of the Iteration Test Plan is to gather all of the information necessary to plan and control the test effort for a given iteration. It describes the approach to testing the software, and is the top-level plan generated and used by managers to direct the test effort.
This Test Plan for the BestPlaces - Project supports the following objectives:
* Decrease and minimise the number of mistakes and bugs
* Provide the users a comfortable and flawless use
* Automated backend and frontend testing

### 1.2	Scope
* Acceptance Testing *
* UI Acceptance Testing with Cucumber

*Data and Database Integrity testing*
* Django will always check if the database ist set up correctly by using its model definitions

*Unit tests*
* Unit Tests in the backend with Django
* Unit Tests in the frontend with JUnit

### 1.3	Intended Audience
* Students
* Professors
* Programmer

### 1.4	Document Terminology and Acronyms
n/a

### 1.5	 References
n/a

### 1.6	Document Structure
tc

## 2.	Evaluation Mission and Test Motivation
Testing provides better usabilty for the user and enables developers to check if their code will work even after something changed.
### 2.1	Background
By testing our project we provide:
* Test if implementation is correct

   Before developing a feature, you'll have to define what it should do. Therefore, you can write a test which checks if the implementation fits the requirements, defined before.
  
* Test the changes

   If you change something in your code, your API or your database, you can check with your unit tests, which were written before the change if all your components can work with this change. If not, you're able to improve your functions by coding till your tests are green

* Deploy only if tests pass

   With automated testing, you're able to check if the application is working properly. Only if everything works, your application will be deployed and public to the real users. So the user always has the guarantee, that the application will worl properly.
   
### 2.2	Evaluation Mission
The goals of testing are the following:

* Software for the user is always stable
* Prevent bugs
* Verify the specification

### 2.3	Test Motivators
* Mrs. Berkling and our grades
* User is happy with the software (no bugs)

## 3.	Target Test Items
The listing below identifies those test items-software, hardware, and supporting product elements -that have been identified as targets for testing. This list represents what items will be tested. 

* UI
* RESTful-API
* Functionality Testing

## 4.	Outline of Planned Tests

### 4.1	Outline of Test Inclusions
* Cucumber UI-Testing
* JUnit-Testing

### 4.2	Outline of Other Candidates for Potential Inclusion
* Dredd-Testing
* User-Testing

### 4.3	Outline of Test Exclusions
* Stress testing (bad server hardware)

## 5.	Test Approach
We commonly will do *integration testing* and *Unit testing*.
### 5.1	Initial Test-Idea Catalogs and Other Reference Sources
n/a
### 5.2	Testing Techniques and Types

#### 5.2.1	Data and Database Integrity Testing
| Technique Objective | Technique | Oracles | Required Tools | Succes Criteria | Special Considerations |
| ------------------- | --------- | ------- | -------------- | --------------- | ---------------------- |
| Testing if the database follows the implementation in the code | Test at startup if the database structure follows the data type definitions in Django | The Backend knows exactly the structure of the database and therefore is able to interact easily with it | Django | No differences between Django models and database models | will be done at every server-start |

#### 5.2.2	Function Testing

| Technique Objective | Technique | Oracles | Required Tools | Succes Criteria | Special Considerations |
| ------------------- | --------- | ------- | -------------- | --------------- | ---------------------- |
| Testing if the UI fits the expectations | Writing feature files, which describe in natural language, how the user will work with the application | The User is happy, that he can use our application | Cucumber, Selenium | All feature file will run flawlessly on our UI | Will run before every deployment |
 
#### 5.2.3	Business Cycle Testing
n/a
 
#### 5.2.4	User Interface Testing

| Technique Objective | Technique | Oracles | Required Tools | Succes Criteria | Special Considerations |
| ------------------- | --------- | ------- | -------------- | --------------- | ---------------------- |
| Let the user click through our application to verify that the usabilty is good enough | Several Users should work with our application for a week to verify everything is working and they can interact with the UI | The User is happy, that he can use our application and it is wasy to use | User | Users will say that they can use our application with ease | Will be done manually by asking different Person to test our application |

## 6.	Entry and Exit Criteria

### 6.1	Test Plan

#### 6.1.1	Test Plan Entry Criteria

#### 6.1.2	Test Plan Exit Criteria

#### 6.1.3	 Suspension and Resumption Criteria

### 6.2	Test Cycles

#### 6.2.1	Test Cycle Entry Criteria

#### 6.2.2	Test Cycle Exit Criteria

#### 6.2.3	Test Cycle Abnormal Termination

## 7.	Deliverables

### 7.1	Test Evaluation Summaries

### 7.2	Reporting on Test Coverage

### 7.3	Perceived Quality Reports

### 7.4	Incident Logs and Change Requests

### 7.5	Smoke Test Suite and Supporting Test Scripts 

### 7.6	Additional Work Products

#### 7.6.1	Detailed Test Results

#### 7.6.2	Additional Automated Functional Test Scripts

#### 7.6.3	Test Guidelines

#### 7.6.4	Traceability Matrices

## 8.	Testing Workflow

## 9.	Environmental Needs

### 9.1	Base System Hardware
The following table sets forth the system resources for the test effort presented in this Test Plan.

System Resources

| Resource | Quantity |	Name and Type |
|--------- | -------- | ------------- |
| Database Server | | |
| Client Test PCs | | |
| Test Repository | | |
| Test Deployment PCs | | |


### 9.2	Base Software Elements in the Test Environment
The following base software elements are required in the test environment for this Test Plan.

| Software Element Name | Version | Type and Other Notes |
| --------------------- | ------- | -------------------- |
| Django | 1.1.0 | - |
| Dredd | 3.5.1 | With API Blueprint |
| JUnit | latest | - |
| Selenium | latest | - |

### 9.3	Productivity and Support Tools
The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name | Vendor or In-house | Version |
| --------------------- | --------------- | ------------------ | ------- |

### 9.4	Test Environment Configurations
The following Test Environment Configurations needs to be provided and supported for this project.

| Configuration Name | Description | Implemented in Physical Configuration |
| ------------------ | ----------- | ------------------------------------- |	

## 10.	Responsibilities, Staffing, and Training Needs

### 10.1	People and Roles
This table shows the staffing assumptions for the test effort.

Human Resources

Have a look at the SRS.

## 11.	Iteration Milestones

Not needed due to Continious Integration.

## 12.	Risks, Dependencies, Assumptions, and Constraints

| Risk | Mitigation Strategy | Contingency (Risk is realized) |
| ---- | ------------------- | ------------------------------ |
| Prerequisite entry criteria is not met. |	<Tester> will define the prerequisites that must be met before Load Testing can start <Customer> will endeavor to meet prerequisites indicated by <Tester>. |<ul><li>	Meet outstanding prerequisites</li><li>Consider Load Test Failure</li></ul>|
| Test data proves to be inadequate.|<Customer> will ensure a full set of suitable and protected test data is available. <Tester> will indicate what is required and will verify the suitability of test data.|<ul><li>Redefine test data</li><li>Review Test Plan and modify	components (that is, scripts)</li><li>	Consider Load Test Failure</li></ul>|
|Database requires refresh.| <System Admin> will endeavor to ensure the Database is regularly refreshed as required by <Tester>.| <ul><li>	Restore data and restart</li><li>Clear Database</li></ul>|

|Dependency between|Potential Impact of Dependency|Owners|
|------------------|------------------------------|------|		

|Assumption to be proven|Impact of Assumption being incorrect|Owners|
|-----------------------|------------------------------------|------|

|Constraint on|Impact Constraint has on test effort|Owners|
|-------------|------------------------------------|------|

## 13.	Management Process and Procedures

### 13.1	Measuring and Assessing the Extent of Testing
To measure how much we test our application, we use Coveralls,io, which is an online test coverage tool. It uses the test runs, which are executed by the Continious Integration Tool Travis CI and by using a plugin for Python and Java we're able to create detailed test reports, which are send to Coveralls. So we always know how good our test coverage is right now and also everybody on our repo is able to see the test coverage, by looking at our coveralls-badge.

### 13.2	Assessing the Deliverables of this Test Plan
n.a.

### 13.3	Problem Reporting, Escalation, and Issue Resolution
If Travis recognises a bug in our software, the corresponding manager is notified directly and he has to resolve the issue.

### 13.4	Managing Test Cycles
As said before all the testing is done either locally while developing or after pushing to the repo, Travis CI will also run tests on their system against it. Afterwards the reports are send to Coveralls, which gives us the ability to improve the test coverage or to see what's gone wrong.

### 13.5	Traceability Strategies

### 13.6	Approval and Signoff

### Results of Coveralls
Just click on the corresponding links to have a look at our Test coverage and also on Travis CI to check if our build is passing:
Travis CI: [Server](https://travis-ci.org/anonfreak/bestplaces-server) [Client](https://travis-ci.org/anonfreak/bestplaces-client)
Coveralls.io: [Server](https://coveralls.io/github/anonfreak/bestplaces-server?branch=master) [Client](https://coveralls.io/github/anonfreak/bestplaces-client?branch=master)

##  Metrics
We also made up our minds about metrics. Therefore, we integrated a metrics tool called codacy, which hooks into our GitHub-project and listens for a push to the Repository. You are able to look at our Metrics stats by accessing it directly on the website or by clicking the badge at our repos. However, here are the links so you don't waster time on searching:

[Server](https://www.codacy.com/app/kolb.marco/bestplaces-server/dashboard)
[Client](https://www.codacy.com/app/kolb.marco/bestplaces-client/dashboard)

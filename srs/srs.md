# Software Requirements Specification 

## Table of contents
- [Table of contents](#table-of-contents)
- [Introduction](#1-introduction)
    - [Purpose](#11-purpose)
    - [Scope](#12-scope)
    - [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [References](#14-references)
    - [Overview](#15-overview)
- [Overall Description](#2-overall-description)
    - [Vision](#21-vision)
    - [Use Case Diagram](#22-use-case-diagram)
	- [Technology Stack](#23-technology-stack)
- [Specific Requirements](#3-specific-requirements)
    - [Functionality](#31-functionality)
    - [Usability](#32-usability)
    - [Reliability](#33-reliability)
    - [Performance](#34-performance)
    - [Supportability](#35-supportability)
    - [Design Constraints](#36-design-constraints)
    - [Online User Documentation and Help System Requirements](#37-on-line-user-documentation-and-help-system-requirements)
    - [Purchased Components](#purchased-components)
    - [Interfaces](#39-interfaces)
    - [Licensing Requirements](#310-licensing-requirements)
    - [Legal, Copyright And Other Notices](#311-legal-copyright-and-other-notices)
    - [Applicable Standards](#312-applicable-standards)
- [Supporting Information](#4-supporting-information)

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) describes all specifications for the application "Common Playground". It includes an overview about this project and its vision, detailed information about the planned features and boundary conditions of the development process.


### 1.2 Scope
The project is going to be realized as an progressive Web App.
  
Actors of this App can be users or guests. 
  
Planned Subsystems are: 
* Dashboard:  
The Dashboard is the main page that shows all the information the user wants to see in a compressed overview.
* Account System:  
Users can create accounts so the configurations they make to their personal dashboard are saved.
* Storing Data:  
User data for accounts has to be stored. The data saved includes tile data, visible / invisible tiles and organisation of those chosen.


### 1.3 Definitions, Acronyms and Abbreviations
| Abbrevation | Explanation                            |
| ----------- | -------------------------------------- |
| SRS         | Software Requirements Specification    |
| UC          | Use Case                               |
| n/a         | not applicable                         |
| tbd         | to be determined                       |
| UCD         | overall Use Case Diagram               |
| FAQ         | Frequently asked Questions             |

### 1.4 References

| Title                                                              | Date       | Publishing organization   |
| -------------------------------------------------------------------|:----------:| ------------------------- |
| [Papatohu Development Blog](http://papatohu.wordpress.com)    | 19.10.2021 | Papatohu Team    |
| [GitHub](https://github.com/papatohu)              		| 19.10.2021 | Papatohu Team    |


### 1.5 Overview
The following chapter provides an overview of this project with vision and Overall Use Case Diagram. The third chapter (Requirements Specification) delivers more details about the specific requirements in terms of functionality, usability and design parameters. Finally there is a chapter with supporting information. 
    
## 2. Overall Description

### 2.1 Vision
Inspired by the lifestyle of traditional Maorians, close to nature and true to their history, we wanted to keep things simple and start with a fresh mindset everyday!
Our application should be a place where you can see all the things that keep your head busy at mornings, all at one glance. The goal is to reduce the need of opening several apps one after another to gather all information that you need starting your day !
### 2.2 Use Case Diagram

![OUCD](../usecase/UseCase.drawio.scope.png)

- Blue = planed not implemented yet
- Green = done
- Purple = partly finished
- Pink = if time remains
- Orange = not till June

### 2.3 Technology Stack
The technology we use is:

Backend:
-Java
-Mongo Database

Frontend:
-Angular

IDE:
-IntelliJ and Webstorm

Project Management:
-Jira
-GitHub

Deployment:
tbd

Testing:
tbd

## 3. Specific Requirements

### 3.1 Functionality
This section will explain the different use cases, you could see in the Use Case Diagram, and their functionality.  
Until December we plan to implement:
- 3.1.1 working foundation (eg. site to add tiles to)
- 3.1.2 Getting an overview
- 3.1.3 Adding a functional tile

Until June, we want to implement:
- 3.1.4 Adding more functional tiles
- 3.1.5 Creating an Account
- 3.1.6 Logging in 
- 3.1.7 Logging out
- 3.1.8 Saving customizations

#### 3.1.1 working foundation
This feature is the essential one of our project. The user has an basic view with the tiles he decides to see, therefore we have to have a container that works and houses these tiles for further custimisation.

[Posting a session](./a) 

#### 3.1.2 Getting an overview
This feature provides a basic overview over all current tiles. All added tiles are shown here. From this overview you can select and customize your experience.
[Session overview](./use_cases/UC3_Session_Overview.md)

#### 3.1.3 Adding a functional tile
This feature provides our first tile that acts as a template for all other tiles during development.

### 3.2 Usability
We plan on designing the user interface as intuitive and self-explanatory as possible to make the user feel comfortable using the app. The UI also shouldn't be too crowded since the information the user wants should be easily readable and not overwhelming to the user.
Though an FAQ document will be available, it should not be necessary to use it.

#### 3.2.1 No training time needed
Our goal is that a user searches up the application, opens it and is able to use all features without any explanation or help.

#### 3.2.2 Familiar Feeling
We want to implement an app with customizable information and layout. This way the user is able to create his own experience that he is comfortable with instead of beeing stuck to one static layout in which information is presented.

### 3.3 Reliability

#### 3.3.1 Availability
Since the Application doesnt communicate with other instances of itself the uptime should be 99% as long as a working version of the application is available. The only thing that can fail is the Database that provides custimizing information so that the user only sees the "guest view" (default layout) when the database is not reachable.

#### 3.3.2 Defect Rate
Our goal is that we have no loss of any data. This is important so that user doesn't feel frustrated loosing the setting he made to improve his experience.

### 3.4 Perfomance

#### 3.4.1 Capacity
The system should be able to manage to run on low computing power devices to make it accessible to as many people as possible.

#### 3.4.2 Storage 
tbd

#### 3.4.3 App perfomance / Response time
To provide the best App perfomance we aim to keep the response time as low as possible. This will make the user experience much better.

### 3.5 Supportability

#### 3.5.1 Coding Standards
We are going to write the code by using all of the most common clean code standards. For example we will name our variables and methods by their functionalities. This will keep the code easy to read by everyone and make further developement much easier.

#### 3.5.2 Testing Strategy
tbd

### 3.6 Design Constraints
We are trying to provide a modern and easy to handle design for the UI aswell as for the architecture of our application. To achieve that the functionalities will be kept as modular as possible.
....ada



explanation of why we choose what and supported platforms
*//
example:
Because we are progamming an Android App we chose Java as our programming language. Also we are using the common MVC-architecture to keep the front end and back end seperated. For a clean front end structure we use MVVM.
To make the communication between the two parts easy, we will implement a RESTful-API between them which will provide the data in JSON-Format. 
The supported Platforms will be:
- Android 4.4 and higher
- Java 8 and higher
//*

### 3.7 On-line User Documentation and Help System Requirements
The usage of the app should be as intuitive as possible so it won't need any further documentation. If the user needs some help we will implement a "Help"-Button in the App which includes a FAQ and a formular to contact the developement team.

### 3.8 Purchased Components
We don't have any purchased components yet. If there will be purchased components in the future we will list them here.

### 3.9 Interfaces

#### 3.9.1 User Interfaces
The User interfaces that will be implented are:
- Dashboard - lists all session and makes it possible to filter sessions
- Customizing View  - shows detailed information about the tiles and makes it possible to (de)activate and move them to your liking
- Login - this page is used to log in 
- Register - provides a registration form
- Profile - makes it possible to post information about yourself
- Settings - shows the settings

#### 3.9.2 Hardware Interfaces
(n/a)

#### 3.9.3 Software Interfaces
tbd

#### 3.9.4 Communication Interfaces
tbd

### 3.10 Licensing Requirements
tbd

### 3.11 Legal, Copyright, and Other Notices
tbd
We do not take responsibilty for any incorrect data or errors in the application.

### 3.12 Applicable Standards
The development will follow the common clean code standards and naming conventions. Also we will create a definition of d which will be added here as soon as its complete.

## 4. Supporting Information
For any further information you can contact the Papatohu Team or check our [Papatohu Development Blog](http://papatohu.wordpress.com). 
The Team Members are:
- Robin Purschwitz
- Dominik Veith
- Rafael Luedtke


<!-- Picture-Link definitions: -->
[OUCD]: https://github.com/IB-KA/CommonPlayground/blob/master/UseCaseDiagramCP.png "Overall Use Case Diagram"

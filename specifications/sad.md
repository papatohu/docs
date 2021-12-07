# Dashup - Software Architecture Document

### Version 2.1

# Revision history

| Date       | Version | Description                                          | Author           |
|------------|---------|------------------------------------------------------|------------------|
| 30/11/2021 | 1.0     | Initial Documentation                                | Fabian Hagner    |


# Table of Contents
- [Introduction](#1-introduction)
    - [Purpose](#11-purpose)
    - [Scope](#12-scope)
    - [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [References](#14-references)
    - [Overview](#15-overview)
- [Architectural Representation](#2-architectural-representation)
- [Architectural Goals and Constraints](#3-architectural-goals-and-constraints)
- [Use-Case View](#4-use-case-view)
- [Logical View](#5-logical-view)
    - [Overview](#51-overview)
    - [Architecturally Significant Design Packages](#52-architecturally-significant-design-packages)
- [Process View](#6-process-view)
- [Deployment View](#7-deployment-view)
- [Implementation View](#8-implementation-view)
    - [Overview](#81-overview)
    - [Layers](#82-layers)
- [Data View](#9-data-view)
- [Size and Performance](#10-size-and-performance)
- [Quality/Metrics](#11-qualitymetrics)

## 1. Introduction

### 1.1 Purpose

This document provides a comprehensive architectural overview of the system, using a number of different architectural 
views to depict different aspects of the system. It is intended to capture and convey the significant architectural 
decisions which have been made on the system.

### 1.2 Scope

This document describes the technical architecture of the Dashup project, including module structure and dependencies as 
well as the structure of classes.

### 1.3 Definitions, Acronyms and Abbreviations

| Abbreviation | Description                            |
| ------------ | -------------------------------------- |
| API          | Application programming interface      |
| MVC          | Model View Controller                  |
| REST         | Representational state transfer        |
| SDK          | Software development kit               |
| SRS          | Software Requirements Specification    |
| UC           | Use Case                               |
| VCS          | Version Control System                 |
| N/A          | Not Applicable                         |
| DAO          | Data Access Object                     |
| DTO          | Data Transfer Object                   |

### 1.4 References

| Reference                                                                             | Date       |
|---------------------------------------------------------------------------------------|------------|
| <a href="https://papatohu.wordpress.com">Papatohu Blog</a>                            | 30/11/2021 |
| <a href="https://github.com/papatohu">GitHub Repository</a>                           | 30/11/2021 |


### 1.5 Overview

This document contains the architectural representation, goals and constraints as well as logical, deployment, 
implementation and data views.

## 2. Architectural Representation

Our project dashup uses the classic Spring Web MVC structure as follows:

<img src="./specifications/image.png" />

## 3. Architectural Goals And Constraints

As our main technology we decided to use Spring Web MVC, which is a framework that takes care of the backend and makes it possible to connect to our frontend which is managed with Angular. 
Besides the controller and model language is Java, so that we do not have to care about 
serialization.
The main architectural goal of this project is portability, distribution and reuse. Since we want our users to customize 
their dashup in any way they want, everything has to be kept abstract and must be made for reuse. 
But of course, the dashup project should be safe as we are storing user sensitive data that should not fall into wrong 
hands.
Architectural constraints for this project might be the interaction with widgets, since we do not allow the user to 
upload executable code for security reasons. So the developer might be limited when it comes to the interaction of the 
user with the developers widgets. But we do accept this limitation, because of the security goal. 

## 4. Use-Case View

This is our overall use-case diagram:

<img src="./usecase/UseCase.drawio.png" alt="Overall use-case diagram" />

## 5. Logical View

### 5.1 Overview



### 5.2 Architecturally Significant Design Packages



## 6. Process View

N/A

## 7. Deployment View


## 8. Implementation View

N/A

## 9. Data View
We chose a MongoDB as our Database, as it fits nicley in our usecase for our user config.
<img src=".dbview/Data View.drawio.png" alt="Model for our Mongo DB" />


## 10. Size and Performance

N/A

## 11. Quality/Metrics



## 12. Patterns


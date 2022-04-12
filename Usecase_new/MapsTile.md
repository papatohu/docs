# 1 Maps tile

The user can define the way to his work / home and can see the current traffic

## 1.1 Brief Description

## 1.1.1 Public

To user has to be logged in to his account to see the website and thus the maps tile.

## 1.1.2 Private

Every registered user can add customized tiles to his screen. One of these tiles can for example be the maps tile. 
The tile can be deactivated in the cofiguration. The user defines the route of which he wants to get the traffic information. 

# 2 Flow of Events

## 2.1 Basic Flow

- User opens the app and the maps tile is visible
- the current traffic for the defined rout is shown
- if nothing is defined, the tile shows a black map
- the user can define a route and the map gets updated to show it


### 2.1.1 Activity Diagram

![Organization Application Activity Diagram](../activityDiagram/Activity%20diagram%20Maps.drawio.png)

### 2.1.2 Mock-up

![Mockup See Weather](https://github.com/papatohu/docs/blob/main/mockups/Maps_tile.png)

<!--
![Create Operation Form Wireframe](../Pictures/Wireframes/CreateOperation.png)
-->

### 2.1.3 Narrative

```gherkin
Feature: see current traffic for entered route

  As a signed in user
  i want to see the current traffic for my way to work

  Background:
    And I am on the homepage

  Scenario: requires a custom route on the database
    if a custom route is found
        call maps-API
            display traffic-information
    else user has to enter a route
        display blanc map
```

## 2.2 Alternative Flows

(n/a)

# 3 Special Requirements

(n/a)

# 4 Preconditions

## 4.1 Login

The user has to be logged in to the system.

# 5 Postconditions

(n/a)

# 6 Extension Points

(n/a)

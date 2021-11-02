# 1 go to Homescreen

The user can go to his personalized homescreen.

## 1.1 Brief Description

Every user can go back to his homescreen.

# 2 Flow of Events

## 2.1 Basic Flow

- User clicks on "Homescreen" button
- System require Config for Users Homescreen
- If custom config found in the Database the config it returns the users config
- If not it returns the standard config
- Render Screen acording to config
- Show rendered Homescreen

### 2.1.1 Activity Diagram

![Activity Diagramm-HomeScreen](https://github.com/papatohu/docs/blob/main/activityDiagram/ActivityDiagramm-HomeScreen.drawio.png)

### 2.1.2 Mock-up

![HomeScreen-loggedIn](https://github.com/papatohu/docs/blob/main/mockups/HomeView_loggedIn.png)

### 2.1.3 Narrative

```
Feature: go back to homescreen
  As a signed in user
  i want to go back to homescreen
  and see my configurated homescreen
  Background:
    And I am on the homepage
  Scenario: require config for user´s homescreen
    If custom config found in the Database the config
        it returns the users config
    else it returns the standard config
    Render Screen acording to config
    Show rendered Homescreen
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


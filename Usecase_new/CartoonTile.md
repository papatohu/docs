# 1 see an Cartoon 

The user can see a new cartoon every day

## 1.1 Brief Description

## 1.1.1 Public

To user has to be logged in to his account to see the website and thus the cartoon.

## 1.1.2 Private

Every registered user can add customized tiles to his screen. One of these tiles can for example be the cartoon. The tile can be deactivated in the cofiguration.

# 2 Flow of Events

## 2.1 Basic Flow

- User opens the app and the cartoon tile is visable
- each day a new cartoon is published, which gets loaded via thier API
- the user can deactivate the tile
- he can no longer see the cartoon, till he activates it again


### 2.1.1 Activity Diagram

![Organization Application Activity Diagram](../activityDiagram/Activity%20diagram%20Cartoon.drawio.png)

### 2.1.2 Mock-up

![Mockup See Weather](https://github.com/papatohu/docs/blob/main/mockups/Cartoon_Tile.png)

<!--
![Create Operation Form Wireframe](../Pictures/Wireframes/CreateOperation.png)
-->

### 2.1.3 Narrative

```gherkin
Feature: see a new cartoon every day

  As a signed in user
  i want to see a new cartoon every day

  Background:
    And I am on the homepage

  Scenario: tile needs to be activated in cofiguration
    if it is set active in config
        call API to get latest cartoon
            display the cartoon
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

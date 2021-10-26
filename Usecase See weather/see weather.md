# 1 see weather

The user can see the weather at his desired location

## 1.1 Brief Description

## 1.1.1 Public

To see the weather at a desired location a user has to be logged in to an account.

## 1.1.2 Private

Every registered user can add customized tiles to his screen. One of these tiles can for example be the weather. To be able to see the weather, the user first has to enter the location to get the weather information from. After that the weather tile shows the weather at the location the user entered befordehand.

# 2 Flow of Events

## 2.1 Basic Flow

- User clicks on "create operation" button
- User fills in the the form
- User clicks on "create" to create the operation, he will be sent to the details view of the operation. A success message will be shown.
- User clicks on "cancel" to close the form without saving the operation.

### 2.1.1 Activity Diagram

![Organization Application Activity Diagram](../Diagrams/UCs/CreateOperationActivityDiagramm.jpg)

### 2.1.2 Mock-up

![Create Operation Form Wireframe](../Pictures/Wireframes/CreateOperation.png)

### 2.1.3 Narrative

```gherkin
Feature: new operation

  As a signed in user
  i want to create a new operation
  and provide additional information regarding my intentions
  in order to find willing helpers.

  Background:
    And I am on the homepage

  Scenario: open new operation dialog
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "main" page
    When I press the "new operation" button
    Then I am on the "new operation" page

  Scenario: enter valid data and save the operation
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "new operation" page
    When I enter "operation XY" in the field "title"
    And I enter "Karlsruhe" in the field "location"
    And I enter "01.01.2018" in the field "date"
    And I enter "public description" in the field "public_descripion"
    And I enter "private description" in the field "private_description"
    And I press the "save" button
    Then I am on the "details" page
    And I receive a "success" message

  Scenario: enter invalid data and save the operation
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "new operation" page
    When I enter "operation XY" in the field "title"
    And I enter "Karlsruhe" in the field "location"
    And I enter "no date" in the field "date"
    And I enter "" in the field "public_descripion"
    And I enter "" in the field "private_description"
    And I press the "save" button
    Then I am on the "new operation" page
    And I receive a "error" message
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

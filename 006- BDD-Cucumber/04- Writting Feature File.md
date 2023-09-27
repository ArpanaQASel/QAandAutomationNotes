## Feature Files: ##

Feature files are written in Gherkin language and define the high-level description of a software feature and its scenarios. Feature files serve as executable documentation and are usually shared among team members.

**Real time Example:(login functionality)**

~~~

Feature: Login Functionality

Scenario: Successful login

Given   the user is on the login page

And     user should have valid credentials to login

When    the user enters valid credentials

Then    the user should be logged in successfully

~~~

Here,

**Feature**      : Overall Functionality which we are going to perform

**Scenarios**    : Particular Scenarios like “Successful login”

**Given**        : Condition before executing program

**When**         : Action which user going to perform

**Then**         : The Output which was came

**And**          : To add Additional Information

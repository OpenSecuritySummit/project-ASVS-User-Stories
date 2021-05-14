# ASVS Requirement: V3.2.1 New session token on user auth

## ASVS:3.2.1

## ASVS Requirement description

Verify the application generates a new session token on user authentication

## User Story

**Feature_Name**: Generation of session tokens on user auth

**Story**:\
As a Security Engineer\
I want to generate new session tokens when users authenticate\
So that I can ensure that attackers can't reuse session tokens

## Scenario

**Scenario_name**: Establishment of session token and invalidation of previous ones

**Gherkin syntax**:

```gherkin
Given a user authentication event
And the need to manage user sessions
Then I create a new session token
And I invalidate any previous active session tokens for that user
```


## External links

<https://cwe.mitre.org/data/definitions/384>
# ASVS Requirement: V3.3.1 Session loguot and expiration
## ASVS:3.3.1

## ASVS Requirement description
Verify that logout and expiration invalidate the session token, such that the back button or a downstream relying party does not resume an authenticated session, including across relying parties.

## User Story

**Feature_Name**: Invalidation of session tokens

**Story**:\
As a Security Engineer\
I want to invalidate session tokens on logout or expiration events\
So that session token values aren't susceptible to re-use

## Scenario

**Scenario_name**: Logout and expiration invalidates the session tokens

**Gherkin syntax**:

```gherkin
Given a user logout event or expiration of a session token
Then I invalidate the session
So that actions requiring user authentication aren't accepted
And I redirect the user to an authentication prompt
```

## External links

<https://cwe.mitre.org/data/definitions/613>
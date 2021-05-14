# ASVS Requirement: V3.3.1 Session loguot and expiration
## ASVS:3.3.1

## ASVS Requirement description
If authenticators permit users to remain logged in, verify that re-authentication occurs periodically both when actively used or after an idle period.

Different assurance levels within ASVS require different parameters:
Level 1: 30 days
Level 2: 12 hours or 30 minutes of inactivity, 2FA optional
Level 3: 12 hours or 15 minutes of inactivity, with 2FA

## User Story

**Feature_Name**: periodic reauthentication

**Story**:\
As a Security Engineer\
I want to permit users to remain logged in for a finite period of time\
So that I can protect the sessions from being re-used

## Scenario

**Scenario_name**: Maximum idle time

**Gherkin syntax**:

```gherkin
Given an active session
When user inactivity exceeeds a defined value
Then I require the user to re-authenticate
```

# NOTE to add 2 scenarios: overall session time and multi-factor authentication
## External links

<https://cwe.mitre.org/data/definitions/613>
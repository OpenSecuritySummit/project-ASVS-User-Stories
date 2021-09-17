# ASVS Requirement: V2.1.11

## ASVS:.2.1.11

## ASVS Requirement description

Verify that "paste" functionality, browser password helpers, and external password managers are permitted

## User Story

**Feature_Name**: enablement of paste functionality for passwords

**Story**:
As a Security Engineer\
I want to allow users to use paste functionality to input passwords
So that they can use password managers effectively when accessing my system

## Scenario

**Scenario_name**: verify paste functionality is usable

**Gherkin syntax**:

```gherkin
Given a password prompt
When the user is expected to input the password
Then pasting is permitted
```

## Validations

**Chef Inspec**

TBC

**OPA**

TBC

**External Tests**

TBC

## External links

<https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html> \
<hhttps://cwe.mitre.org/data/definitions/521.html>

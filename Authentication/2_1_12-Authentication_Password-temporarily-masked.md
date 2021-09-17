# ASVS Requirement: V2.1.12

## ASVS:.2.1.12

## ASVS Requirement description

Verify that the user can choose to either temporarily view the entire masked password, or temporarily view the last typed character of the password on platforms that do not have this as built-in functionality.

## User Story

**Feature_Name**: View entire masked password

**Story**:
As a Security Engineer\
I want to allow users to temporarily view their masked password
So that my system is made more accessible to users with different needs

## Scenario

**Scenario_name**: Masked password can be viewed unmasked

**Gherkin syntax**:

```gherkin
Given a password prompt
And the password prompt masks the user's password
When the user wants to check the unmasked password
Then they click on a button to trigger the unmasking
And the password is shown unmasked
```
**Scenario_name**: Masked password can be viewed unmasked

**Gherkin syntax**:

```gherkin
Given a password prompt
And the password prompt masks the user's password
And the platform doesn't support unmasking
When the user wants to check the unmasked password
Then they click on a button to trigger the unmasking
And the last typed character is shown
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

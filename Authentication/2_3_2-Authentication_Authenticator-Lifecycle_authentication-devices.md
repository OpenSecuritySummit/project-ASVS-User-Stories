# ASVS Requirement: V2.3.2

## ASVS:.2.3.2

## ASVS Requirement description

Verify that enrollment and use of subscriber-provided authentication devices are supported, such as a U2F or FIDO tokens.

## User Story

**Feature_Name**: enrollment and use of authentication devices (U2F and FIDO)

**Story**:
As a Security Engineer\
I want users to be able to use their own authentication devices\
So that we enable them 

## Scenario

**Scenario_name**: enroll user-provided authentication device

**Gherkin syntax**:

```gherkin
Given a user registration event
When request information from the user to setup security credentials
Then I request a username and password pair
And I provide the ability for the user to enroll an authentication device
```

`authentication device` in this context relates to U2F or FIDO tokens

**Scenario_name**: authenticate using authentication device

**Gherkin syntax**:

```gherkin
Given a user login event
And a user with authentication device enabled
When I request information from the user
Then I ask for a username and password pair
And I request the credentials from the token
Then I confirm that the credentials are valid
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
<hhttps://cwe.mitre.org/data/definitions/330.html>
<https://pages.nist.gov/800-63-3/sp800-63b.html> 5.1.1.2 / A3


# ASVS Requirement: V2.3.1

## ASVS:.2.3.1

## ASVS Requirement description

Verify system generated initial passwords or activation codes SHOULD be securely randomly generated, SHOULD be at least 6 characters long, and MAY contain letters and numbers, and expire after a short period of time. These initial secrets must not be permitted to become the long term password.

## User Story

**Feature_Name**: initial system password for users

**Story**:
As a Security Engineer\
I want users to be initially assigned a temporary and secure password\
So that the initial logon is not compromised

## Scenario

**Scenario_name**: construction of initial system password

**Gherkin syntax**:

```gherkin
Given a user registration event
When I set an initial password or activation code for the user
Then I generate it securely and randomly
And I enforce a minimum password length of 6 characters
And I set it to expire after X min
And I don't allow this initial password to be used for more than X days

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


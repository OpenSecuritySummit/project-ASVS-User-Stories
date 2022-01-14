# ASVS Requirement: V2.2.5

## ASVS:.2.2.5

## ASVS Requirement description

Verify that where a credential service provider (CSP) and the application verifying authentication are separated, mutually authenticated TLS is in place between the two endpoints.

## User Story

**Feature_Name**: encrypted comms between application and credential service provider

**Story**:
As a Security Engineer\
I want encrypt communications between my application and my credential service provider\
So that prevent man-in-the-middle attacks which could expose credentials

## Scenario

**Scenario_name**: encryption of authentication traffic

**Gherkin syntax**:

```gherkin
Given the need to authenticate users
When users login
Then I verify credentials against my credential service provider
And I ensure that the traffic is TLS protected
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
<hhttps://cwe.mitre.org/data/definitions/319.html>
<https://pages.nist.gov/800-63-3/sp800-63b.html> 5.2.6

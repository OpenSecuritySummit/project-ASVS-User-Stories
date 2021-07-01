# ASVS Requirement: V13.1.4 Authorization decisions made at both URI and resource level

## ASVS:13.1.4

## ASVS Requirement description

Verify that authorization decisions are made at both the URI, enforced by programmatic or declarative security at the controller or router, and at the resource level, enforced by model-based permissions

## User Story

**Feature_Name**: Authorization decision made at the URI and resource level

**Story**:\
As a Security Engineer\
I want to verify that authorization decisions are made at both the URI and resource level
So that I can prevent opportunities for unauthorised access to a given resource

## Scenario

**Scenario_name**: Authorization decision made at the URI

**Gherkin syntax**:

```gherkin
Given a resource requiring protection
When I access the resource
Then I verify the authorization decision at the URI
And I notify the service of sucessfull access attempt
```


## Validations

**Chef Inspec**

TBC

**OPA**

TBC

**External Tests**

TBC

## External links

<https://cheatsheetseries.owasp.org/cheatsheets/Web_Service_Security_Cheat_Sheet.html>
<https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html>
<https://cwe.mitre.org/data/definitions/598>

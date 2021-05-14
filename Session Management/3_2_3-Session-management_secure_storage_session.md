# ASVS Requirement: V3.2.3 Secure session storage in browser 
## ASVS:3.2.1
# NOTE: This particular document needs to be reviewed.

## ASVS Requirement description

Verify the application only stores session tokens in the browser using secure methods such as appropriately secured cookies (see section 3.4) or HTML 5 session storage.

NOTE: Our interpretation of this requirement is that it refers to session persistence. More details on cookie security will be in section 3.4

## User Story

**Feature_Name**: Secure session storage in the browser

**Story**:\
As a Security Engineer\
I want to ensure that session tokens stored in cookies or session storage cannot be retrieved once session is ended\
So that session tokens cannot be exploited or re-used by other parties

## Scenario

**Scenario_name**: 

**Gherkin syntax**:

```gherkin
Given the creation of a session token
When I instruct the browser to store the session token
Then I use a mechanism with is non-permanent
So that the session token is not retained
```


## External links

https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html
<https://cwe.mitre.org/data/definitions/331>
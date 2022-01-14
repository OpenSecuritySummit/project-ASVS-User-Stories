# ASVS Requirement: V2.2.7

## ASVS:.2.2.7

## ASVS Requirement description

Verify intent to authenticate by requiring the entry of an OTP token or user-initiated action such as a button press on a FIDO hardware key.

## User Story

**Feature_Name**: confirmation of user intent for authentication

**Story**:
As a Security Engineer\
I want users to confirm physical device input before authenticating them\
So that I have confirmation that the user is physically present during the authentication process

## Scenario

**Scenario_name**: confirmation of user intent through physical presence verification

**Gherkin syntax**:

```gherkin
Given the need to authenticate users
When the user starts the login process
Then I authenticate them using available methods
And I require the user to prove physical presence
```

Proving physical presence can be done through an OTP token or through pressing a button on a FIDO hardware key

## Validations

**Chef Inspec**

TBC

**OPA**

TBC

**External Tests**

TBC

## External links

<https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html> \
<hhttps://cwe.mitre.org/data/definitions/308.html>
<https://pages.nist.gov/800-63-3/sp800-63b.html> 5.2.9

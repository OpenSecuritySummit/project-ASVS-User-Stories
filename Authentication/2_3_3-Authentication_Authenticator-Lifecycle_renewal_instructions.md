# ASVS Requirement: V2.3.3

## ASVS:.2.3.3

## ASVS Requirement description

Verify that renewal instructions are sent with sufficient time to renew time bound authenticators

## User Story

**Feature_Name**: send authenticator renewal instructions

**Story**:
As a Security Engineer\
I want to notify my users when their time bound authenticators are about to expire\
So that the user doesn't lose access to my services due to expired authenticators

NOTE: this requirement is somewhat *strange* as ASVS seems to refer to time-bound authenticators (so assuming it's related to token that have an expiry date on them, not the usual Authenticator apps which don't usually have a time-limit) but the NIST reference (6.1.4) says "The CSP SHOULD bind an updated authenticator an appropriate amount of time before an existing authenticator’s expiration.", which seems to suggest it relates to the time window between the token code changing and being useful/valid for the authentication process itself. I don't think they're the same. The assumption for the first scenario is that the token itself has a due-date and the second scenario has the assumption that we're managing the login process and validity of the challenge itself

## Scenario

**Scenario_name**: send authenticator renewal notification

**Gherkin syntax**:

```gherkin
Given a user login
And the user has token authentication enabled
When I request information from the user
Then I request a username and password pair
And I request the credentials from the authenticator app
Then I confirm that the credentials are valid
And I check if the authenticator will expire in the next X weeks
Then I notify the user that his credentials are about to expire and they should change it
```

**Scenario_name**: ensure authenticator credentials are valid

**Gherkin syntax**:

```gherkin
Given a user login
And the user has token authentication enabled
When I request information from the user
Then I request a username and password pair
And I request the credentials from the authenticator app
Then I verify that the authenticator code is used within X seconds of its timestamp
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
<hhttps://cwe.mitre.org/data/definitions/287.html>
<https://pages.nist.gov/800-63-3/sp800-63b.html> 6.1.4


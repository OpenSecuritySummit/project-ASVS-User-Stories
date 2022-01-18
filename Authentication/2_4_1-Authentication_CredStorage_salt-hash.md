# ASVS Requirement: V2.4.1

## ASVS:.2.4.1

## ASVS Requirement description

Verify that passwords are stored in a form that is resistant to offline attacks. Passwords SHALL be salted and hashed using an approved one- way key derivation or password hashing function. Key derivation and password hashing functions take a password, a salt, and a cost factor as inputs when generating a password hash

## User Story

**Feature_Name**: credential storage using one way hashing functions

**Story**:
As a Security Engineer\
I want to store credentials securely using one-way hash functions\
So that I protect my user credentials from offline attacks


## Scenario

**Scenario_name**: send authenticator renewal notification

**Gherkin syntax**:

```gherkin
Given a password change or password setting event
When I store the password
Then I add a random salt
And I use a secure one-way key derivation or password hashing function
And I add a cost factor of X to this computation
Then I store it in a secure location with strong access control measures
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
<hhttps://cwe.mitre.org/data/definitions/916.html>
<https://pages.nist.gov/800-63-3/sp800-63b.html> 5.1.1.2


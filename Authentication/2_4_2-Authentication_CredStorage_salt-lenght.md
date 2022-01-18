# ASVS Requirement: V2.4.2

## ASVS:.2.4.2

## ASVS Requirement description

Verify that the salt is at least 32 bits in length and be chosen arbitrarily to minimize salt value collisions among stored hashes. For each credential, a unique salt value and the resulting hash SHALL be stored

## User Story

**Feature_Name**: salt length for password storage

**Story**:
As a Security Engineer\
I want to ensure the salt value used is sufficiently random\
So that I can minimize salt value collisions among stored hashes


## Scenario

**Scenario_name**: verification of salt length

**Gherkin syntax**:

```gherkin
Given a password change or password setting event
When I store the password
Then I add a random salt of at least 32 bits generated randomly
And I store a unique salt value and the resulting hash
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


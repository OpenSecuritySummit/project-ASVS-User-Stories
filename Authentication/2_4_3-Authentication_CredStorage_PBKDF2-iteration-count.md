# ASVS Requirement: V2.4.3

## ASVS:.2.4.3

## ASVS Requirement description

Verify that if PBKDF2 is used, the iteration count SHOULD be as large as verification server performance will allow, typically at least 100,000 iterations

## User Story

**Feature_Name**: secure implementation of PBKDF2

**Story**:
As a Security Engineer\
I want to ensure that when I use PBKDF2 I define a large enough iteration count\
So that I can ensure the stored hashes are securely randomised to decrease chances of collisions and disclosure


## Scenario

**Scenario_name**: verify PBKDF2 implementation

**Gherkin syntax**:

```gherkin
Given a password change or password setting event
And I'm using PBKDF2 derivation functions
When I store the password
Then I add a random salt of at least 32 bits generated randomly
And I set an iteration count of at least 100.000
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


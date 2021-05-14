# ASVS Requirement: V3.2.2 New session token on user auth

## ASVS:3.2.1

## ASVS Requirement description

Verify that session tokens possess at least 64 bits of entropy

## User Story

**Feature_Name**: Sufficient entropy for session tokens

**Story**:\
As a Security Engineer\
I want to generate session tokens with at least 64 bits of entropy\
So that session token values aren't predictable

## Scenario

**Scenario_name**: Validation of minimum entropy in session token generation

**Gherkin syntax**:

```gherkin
Given the creation of a session token
When I create a random string for the session token value
Then I ensure that the random string generated uses entropy
And that this entropy is at least 64 bits long
```


## External links

<https://cwe.mitre.org/data/definitions/331>
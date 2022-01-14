# ASVS Requirement: V2.2.4

## ASVS:.2.2.4

## ASVS Requirement description

Verify impersonation resistance against phishing, such as the use of multi-factor authentication, cryptographic devices with intent (such as connected keys with a push to authenticate), or at higher AAL levels, client-side certificates.

## User Story

**Feature_Name**: impersonation resistance against phishing

**Story**:
As a Security Engineer\
I want to verify my application's resistance to impersonation attacks\
So that I have assurance that my users are who they claim to be

## Scenario

**Scenario_name**: enable multi-factor authentication

**Gherkin syntax**:

```gherkin
Given the need to authenticate users
When users login
Then I authenticate them using username/password pair
And I authenticate users with a second factor
```

`second factor` can be OTP (one time password), magic links, authenticator app codes or QR codes

**Scenario_name**: enable client-side TLS authentication

**Gherkin syntax**:

```gherkin
Given the need to authenticate users
When users login
Then I authenticate them using username/password pair
And I validate a client-side certificate provided by the user
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
<hhttps://cwe.mitre.org/data/definitions/308.html>
<https://pages.nist.gov/800-63-3/sp800-63b.html> 5.2.5
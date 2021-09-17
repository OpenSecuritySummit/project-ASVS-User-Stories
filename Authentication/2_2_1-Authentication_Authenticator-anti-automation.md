# ASVS Requirement: V2.2.1

## ASVS:.2.2.1

## ASVS Requirement description

Verify that anti-automation controls are effective at mitigating breached credential testing, brute force, and account lockout attacks. Such controls include blocking the most common breached passwords, soft lockouts, rate limiting, CAPTCHA, ever increasing delays between attempts, IP address restrictions, or risk-based restrictions such as location, first login on a device, recent attempts to unlock the account, or similar. Verify that no more than 100 failed attempts per hour is possible on a single account.

## User Story

**Feature_Name**: anti-automation controls against authentication requests

**Story**:
As a Security Engineer\
I want to implement anti-automation controls\
So that my system is protected against successful authentication attacks

## Scenario

**Scenario_name**: validate effectiveness of anti-automation capabilities presented to users

**Gherkin syntax**:

```gherkin
Given a login page
And I present a login screen
When the user introduces login credentials
And I present them with an anti-automation measure
Then I validate the results of the measure
And allow access if the credentials are valid
```

**Scenario_name**: validate effectiveness of anti-automation capabilities enforced by the system

**Gherkin syntax**:

```gherkin
Given a login page
And I present a login screen
When the user introduces login credentials
Then I assess the threat posed by the request
And I apply `anti-automation` mechanisms
And only allow user to authenticate if criteria implemented by the mechanisms is met
And I raise an event in respect to this event
```

`anti-automation` mechanisms enforced by the system can be one or more of  breached credential testing, account lockouts, rate limiting, soft lockout, risk-based restrictions such as location, blocking of IP addresses

## Validations

**Chef Inspec**

TBC

**OPA**

TBC

**External Tests**

TBC

## External links

<https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html> \
<hhttps://cwe.mitre.org/data/definitions/521.html>

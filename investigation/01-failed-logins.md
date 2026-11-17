# Investigation 01: Failed Logon Attempts

## Objective
Identify repeated failed logon attempts in the simulated Windows security dataset.

## Query Used
The KQL query filtered for Event ID 4625 and grouped the results by account and source IP address.

## Finding
The query identified:

- Account: `admin`
- Source IP: `198.51.100.25`
- Failed attempts: 4

A successful logon involving the same account and source IP was also recorded shortly after the failed attempts.

## Analyst Observation
Repeated failed logon attempts followed by a successful logon may indicate possible password guessing or unauthorised access.

However, this activity alone does not confirm that the account was compromised.

## Recommended Next Step
Review the successful logon and verify whether the activity was expected and authorised. Additional evidence would be required before reaching a conclusion.

## Investigation Status
Flagged for further review.

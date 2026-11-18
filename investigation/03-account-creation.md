# Investigation 03: Account Creation Analysis

## Objective
Review account creation events within the simulated Windows security dataset.

## Finding
The query identified one account creation event:

- Event ID: 4720
- Account: newuser
- Computer: WORKSTATION-01
- Source IP: 192.0.2.15
- Timestamp: 08:15

## Analyst Observation
The account creation event warrants further investigation because it occurred within a dataset that also contains suspicious logon and privileged activity.

Although the source IP is the same as the earlier jsmith logon, the available evidence does not establish that jsmith created the account.

## Recommended Next Steps
- Confirm whether the new account creation was authorised.
- Establish who initiated the account creation.
- Review the account's assigned permissions.
- Determine whether the new account was subsequently used to log on.
- Investigate any activity performed by the account after creation.

## Investigation Status
Account creation identified. Authorisation and account ownership remain unverified.

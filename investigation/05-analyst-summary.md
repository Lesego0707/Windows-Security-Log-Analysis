# Analyst Summary & Conclusion

## Investigation Overview

This investigation reviewed a simulated Windows security dataset using Kusto Query Language (KQL) in Azure Data Explorer.

The analysis focused on failed logon attempts, successful logons, account creation, and special privileges events to identify activity that may require further investigation.

## Key Findings

### 1. Repeated Failed Logons
Four consecutive failed logon attempts involving the `admin` account were observed from `198.51.100.25` between 08:05 and 08:08.

### 2. Successful Logon Following Failed Attempts
At 08:09, a successful logon involving the same `admin` account and source IP was recorded.

The sequence raises suspicion of possible password guessing but does not confirm that an attack occurred.

### 3. Account Creation
At 08:15, an account creation event involving `newuser` was recorded from `192.0.2.15`.

The available data does not identify who initiated the account creation or whether it was authorised.

### 4. Special Privileges
At 08:20, an event involving special privileges assigned to the `admin` account was recorded from `192.0.2.15`.

The event requires further review to establish whether the privileged logon was expected and what activity followed.

## Analyst Assessment

The simulated events contain activity that warrants further investigation, particularly the repeated failed logons followed by a successful logon involving the same admin account.

Account creation and special privileges events also raise questions about authorisation and account activity.

Although the events share source IP addresses, the dataset does not establish that they were performed by the same person or belong to the same session.

No confirmed compromise can be concluded from the available evidence.

## Recommended Actions

- Validate the successful admin logon against approved access and activity.
- Investigate the repeated failed logon attempts.
- Confirm whether the creation of `newuser` was authorised.
- Review the privileges associated with the admin logon.
- Determine whether the newly created account was subsequently used.
- Examine additional security logs to establish the sequence of events and identify the responsible account or user.
- Escalate for further investigation if unauthorised activity is identified.

## Conclusion

The investigation identified suspicious patterns in the simulated Windows security events, including repeated failed logons followed by a successful logon, account creation, and special privileges activity.

These findings highlight the importance of monitoring authentication events and reviewing account-related activity.

Further evidence would be required to determine whether the events were connected, authorised, or indicative of a security incident.

## Investigation Outcome

**Status:** Suspicious activity identified — further investigation required.

**Scope:** Eight synthetic security events.

**Environment:** Azure Data Explorer using KQL.

**Limitation:** This exercise uses simulated data and does not represent a real security incident or confirmed compromise.

# Investigation 04: Privileged Activity Analysis

## Objective
Review events involving the assignment of special privileges to identify activity that may require further investigation.

## Finding
The query identified one special privileges event:

- Event ID: 4672
- Account: admin
- Computer: WORKSTATION-01
- Source IP: 192.0.2.15
- Timestamp: 08:20
- Activity: Special privileges assigned

## Analyst Observation
The event indicates that special privileges were associated with the admin logon.

The activity warrants further investigation to determine whether the logon and privileges were expected and authorised.

Although the event shares a simulated source IP with the earlier jsmith logon and account creation event, the available dataset does not establish that these activities were performed by jsmith or that they belong to the same session.

## Recommended Next Steps
- Verify whether the admin logon was authorised.
- Review the privileges associated with the event.
- Establish who was using the admin account at the time.
- Review subsequent activity performed during the privileged session.
- Investigate additional logs for evidence of unauthorised activity.

## Investigation Status
Special privileges event identified. Authorisation and associated activity remain unverified.

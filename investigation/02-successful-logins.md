# Investigation 02: Successful Logon Analysis

## Objective
Review successful logon events and identify activity that may require further investigation.

## Finding

The query identified two successful logon events:

- `jsmith` successfully logged in at 08:00 from `192.0.2.15`.
- `admin` successfully logged in at 08:09 from `198.51.100.25`.

The admin logon followed four consecutive failed logon attempts involving the same account and simulated source IP.

## Analyst Observation

The successful admin logon following repeated failures raises suspicion of possible password guessing or unauthorised access.

The subsequent account creation and special privileges events associated with `192.0.2.15` also warrant further review.

Questions requiring further investigation include:

- Was the admin logon expected and authorised?
- What is the role of the jsmith account?
- Was the account creation event approved?
- Was the privileged activity expected?
- Can additional evidence establish who performed these actions?

The available dataset does not establish that jsmith performed the account creation or privileged activity.

## Recommended Next Steps

- Verify whether the successful admin logon was legitimate.
- Review the account creation event and confirm authorisation.
- Investigate the context of the special privileges event.
- Obtain additional logs to establish the responsible account or user.

## Investigation Status
Suspicious activity identified. Further investigation required.

# Entra-employee-portal-access-lab
A Microsoft Entra ID Free lab testing employee portal sign-in, application assignments, and denied access.
# Employee Portal Access Control with Microsoft Entra ID

## Status
In progress — personal learning lab.

## Objective
Configure Microsoft Entra sign-in for a test employee portal
and verify that only assigned users can access it.

## Business scenario
Adera Technologies is a fictional company.
Its employee portal should allow assigned employees to sign in
and deny access to unassigned users.

## Tools
- Microsoft Entra ID Free
- A test employee portal
- GitHub for technical documentation
- Medium for the completed project walkthrough

## Planned tests
1. An assigned employee can sign in.
2. An unassigned employee is denied access.
3. After assignment removal, a fresh sign-in is denied.

## Licence scope
This lab will use individual user assignments.
Group-based application assignment requires a premium licence.

## Progress
- Created this repository.
- Application setup and access testing are not yet documented
  as completed.

## Evidence plan
For each activity, record:
- The requirement and reason for the change.
- ## Activity 1 — Register the application

### Business requirement
Prepare an application to use sign-in through our lab directory.

### Actions completed
Registered Adera Employee Portal Lab as a single-tenant application.

### Verification
Opened the application's Overview page and confirmed:
- Display name: Adera Employee Portal Lab
- Supported account types: Single tenant

### Current limitations
The portal has not been built.
Redirect URI, user assignments, and sign-in tests are pending.

### What I learned
App registration establishes the application's identity in Entra.
It does not create or host the portal.
- Configuration steps actually completed.
- Expected and observed test results.
- Screenshots with personal information removed.
- Troubleshooting and testing limitations.
- - Confirmed Supported account types shows “My organization only.”
  - 
  - ## Activity 2 — Configure the redirect URI

### Actions completed
Added a Single-page application platform with this redirect URI:
http://localhost:3000/

### Verification
Confirmed the URI remained listed after refreshing
the Authentication page.

### What I learned
The redirect URI is where Entra returns the browser
after authentication.

### Testing status
The portal is not running yet. Sign-in has not been tested.
## Activity 3 — Require application assignment

### Change
Set “Assignment required?” to Yes for Adera Employee Portal Lab.

### Verification
Refreshed Properties and confirmed the setting remained Yes.

### Purpose
Require an application assignment before a user can sign in.

### Testing status
Allowed and denied sign-in tests are still pending.

## Activity 4 — Assign the test user

### Actions completed
- Created Portal Allowed and Portal Unassigned as ordinary users.
- Assigned only Portal Allowed to Adera Employee Portal Lab.

### Verification
Checked the application's Users and groups list:
- Portal Allowed was listed.
- Portal Unassigned was absent.

## Testing status
- Assigned-user sign-in: Passed.
- Unassigned-user sign-in: Passed — AADSTS50105.
- Sign-in after assignment removal: Pending.

## Test 1 — Assigned user

- User: portal.allowed
- Application assignment: Present
- Expected: Successful sign-in
- Observed: Returned to the portal as portal.allowed
- Result: Pass
- ## Test 2 — Unassigned user

- User: portal.unassigned
- Application assignment: Absent
- Expected: Sign-in denied because assignment is required
- Observed: Entra returned AADSTS50105, explicitly stating
  that the user lacked an application assignment
- Result: Pass
- Test time: 2026-09-12 08:57:40 UTC
- 

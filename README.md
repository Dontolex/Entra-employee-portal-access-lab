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

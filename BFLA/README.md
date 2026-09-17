# BFLA – Unauthorised Actions Performed by User

## Overview
Brief explanation of the vulnerability and what was discovered.

The BFLA vulnerability discovered in this section. 
 An authenticated, low-privilege user can abuse an administrative endpoint to delete video files belonging to any other platform user. Initially, unauthorized deletion attempts returned a verbose error message leaking hidden internal API routing components. Because the backend fails to validate user roles on administrative functions, standard users can invoke this hidden path to perform restricted, highly destructive actions (Vertical Privilege Escalation).

## Target
crAPI API Security Lab

## Vulnerability
BFLA / OWASP API5:2023

## What I Discovered
By using the verbose error message on from an atttempted attack, intel 
suggested that was ADMIN permissions were required to perform "DELETE" action on crAPI. 
However, in order to exploit this vulnerability in the real world, you would need to retrieve a valid resource identifier 
integer that points to another users video and this can be done with a Burp Inspector.


## Tools
- Burp Suite
- Postman

## Attack Flow
User A → GET request → Change resource ID → API returns User B's data

## Evidence
[Screenshot 1]
[Screenshot 2]

## Impact
 Unauthorized data deletion breaches system data integrity and directly compromises availability for legitimate users.

## Remediation
Deny access by default to any API path prefixed with /admin/ unless the user session explicitly satisfies administrative policy criteria at the API gateway tier.

## Detailed Report
[View Full BFLA Report](./report/BFLA-Report.pdf)

# BOLA – Unauthorized Access to Other Users' Mechanic Reports

## Overview
Brief explanation of the vulnerability and what was discovered.

There are two BOLA vulnerabilities discovered in this section. 
Finding 1- This vulnerability was exploited through manipulating the Resource ID in the URL path. The API 
endpoint handles access control poorly by determining which mechanic report to display based
solely on a sequential ID parameter passed in the URL path, failing to verify whether the
authenticated user owns that specific resource.

Finding 2-  The crAPI store allows users to cancel purchases using an HTTP DELETE method. 
However, the server lacks authorization validation on this method, relying entirely on the 
client-supplied order_id string in the URL path.


## Target
crAPI API Security Lab

## Vulnerability
BOLA / OWASP API1:2023

## What I Discovered
Finding 1 - By modifying the resource ID in a GET request, I was able
to access another user's mechanic report and associated PII.

Finding 2 - 

## Tools
- Burp Suite
- Postman

## Attack Flow
User A → GET request → Change resource ID → API returns User B's data

## Evidence
[Screenshot 1]
[Screenshot 2]

## Impact
Unauthorized access to another user's information.

## Remediation
Implement server-side object-level authorization checks.

## Detailed Report
[View Full BOLA Report](./report/BOLA-Report.pdf)

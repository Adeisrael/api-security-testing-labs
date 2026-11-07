# API SECURITY TESTING LAB

# OVERVIEW 

This project documents practical API security testing techniques, methodologies, vulnerabilities, and remediation strategies. 

The objective is to develop a structured understanding of API attack surfaces and demonstrate practical application security testing skills using controlled lab environments.  

# Objectives
- Understand common API attack surfaces according to OWASP
- Assess authentication mechanisms
- Test authorisation controls
- Identify input validation weaknesses
- Investigate API security vulnerabilities
- Understand common API attack techniques
- Document security findings
- Develop appropriate remediation recommendations

# Technologies & Tools
<li>Burp Suite
<li>Postman
<li>Kali Linux
<li>Git
<li>Python

  
# Testing Areas
### 1. Authentication

Testing the mechanisms used to verify the identity of API users.

Areas of investigation include:
<li>Authentication bypass
<li>Weak authentication mechanisms
<li>Token handling
<li>Session management
<li>JWT security<br/>

  
### 2. Authorization

Testing whether authenticated users can access resources they should not be permitted to access.

Areas of investigation include:
<li>Broken access control
<li>BOLA
<li>Privilege escalation
<li>Horizontal privilege escalation
<li>Vertical privilege escalation

### 3. Input Validation

Testing how APIs process and validate user-controlled input.

Areas of investigation include:
<li>Parameter manipulation
<li>Injection vulnerabilities
<li>Unexpected input
<li>Data-type manipulation
<li>Server-side validation
  
### 4. Business Logic

Investigating whether application functionality can be abused in unintended ways.
<br/>

### 5. API Enumeration

Identifying available:
<li>Endpoints
<li>Parameters
<li>HTTP methods
<li>API versions
<li>Authentication mechanisms

# Methodology
  The testing methodology follows a structured process:

<li>Reconnaissance
<li>API enumeration
<li>Attack-surface identification
<li>Authentication testing
<li>Authorization testing
<li>Input validation testing
<li>Business-logic testing
<li>Vulnerability validation
<li>Risk assessment
<li>Remediation analysis
<li>Documentation
  
# Lab Environment

All testing was performed against intentionally vulnerable applications in controlled lab environments. 

No confidential client, employer, production, or proprietary information is included in this repository.

# Findings

Security findings will be documented according to:
<li>Vulnerability
<li>Description
<li>Severity
<li>Affected functionality
<li>Reproduction steps
<li>Security impact
<li>Evidence
<li>Recommended remediation

Where vulnerabilities are identified, the project will document appropriate defensive measures and secure implementation recommendations.

### Completed Reports
| ID | Vulnerability Class | Severity | Status |
|----|--------------------|----------|--------|
| 01 | BOLA — object access across user boundaries | High | Report complete |
| 02 | BFLA — unauthorised function invocation | High | Report complete |

# Learning Outcomes

This work demonstrates practical understanding of API security, web application security, authentication, authorization, vulnerability assessment, security testing methodology, security documentation, and risk-based remediation.

# Limitations

<li>Tests were performed in confined lab environments; no production or live-target validation was performed.
<li>Coverage is weighted toward authorization flaws (BOLA/BFLA); injection and business-logic testing are less developed.
<li>Findings were manually validated; no automated fuzzing or regression harness was built.

#Future Work
<li>Automated API security testing and Python-based security tooling
<li>Machine-learning-assisted vulnerability analysis
<li>AI-assisted security testing
<li>LLM security testing


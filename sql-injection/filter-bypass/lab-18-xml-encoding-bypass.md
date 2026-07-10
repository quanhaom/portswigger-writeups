# Lab: SQL Injection with Filter Bypass via XML Encoding

## Overview

This lab demonstrates how input filtering mechanisms can sometimes be circumvented through alternative data representations. It highlights the limitations of relying solely on filtering controls to prevent injection vulnerabilities.

## Root Cause

The application depends on input filtering rather than addressing the underlying vulnerability. User-controlled data reaches database queries without adequate parameterization, allowing injection risks to remain present.

## Key Concepts

* SQL Injection
* Input filtering limitations
* Data encoding
* Defense-in-depth

## Impact

Potential consequences include:

* Circumvention of security controls
* Exposure of sensitive information
* Increased attack surface
* Reduced effectiveness of filtering mechanisms

## Detection Summary

Testing indicated that application filtering controls did not fully account for alternative input representations, allowing database query behavior to be influenced.

## Remediation

* Use parameterized queries
* Avoid relying solely on blacklist filtering
* Validate data according to expected formats
* Implement layered security controls

## Lessons Learned

* Filtering alone is not a complete defense against SQL Injection.
* Secure query construction is more effective than attempting to block malicious input patterns.
* Defense-in-depth provides stronger protection than any single control.

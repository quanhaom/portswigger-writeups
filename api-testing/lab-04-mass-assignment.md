# Lab: Exploiting a Mass Assignment Vulnerability

## Overview

This lab demonstrates how automatic binding of user-supplied data to application objects can introduce security vulnerabilities when sensitive fields are insufficiently protected.

## Root Cause

The application accepts more user-controlled properties than intended and automatically maps them to backend objects without proper restrictions.

## Key Concepts

* Mass Assignment
* API Security
* Object Mapping
* Authorization Controls

## Impact

Potential consequences include:

* Unauthorized privilege modification
* Manipulation of sensitive attributes
* Business logic abuse
* Access control violations

## Detection Summary

Assessment activities revealed that backend object properties could be influenced through API requests beyond the intended functionality.

## Remediation

* Use allowlists for accepted fields
* Restrict sensitive object properties
* Implement server-side authorization checks
* Review object mapping frameworks

## Lessons Learned

* Automatic object binding introduces security risk.
* Authorization must be enforced independently of user input.
* Sensitive fields should never be implicitly trusted.

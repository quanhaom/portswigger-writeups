# Lab: DOM XSS Using Web Messages and JSON.parse

## Overview

This lab demonstrates how client-side parsing and processing of structured data can create security risks when untrusted input is treated as trusted application data.

## Root Cause

The application receives externally supplied data, parses it, and uses the resulting values within application logic without adequate security validation.

## Key Concepts

* DOM-based XSS
* Structured data processing
* Client-side trust boundaries
* Browser security

## Impact

Potential consequences include:

* Script execution
* Data exposure
* Session compromise
* Manipulation of application behavior

## Detection Summary

Security testing revealed that parsed client-side data influenced DOM operations in a manner that introduced security risk.

## Remediation

* Validate parsed data
* Sanitize all untrusted values
* Use safe DOM update methods
* Implement CSP protections

## Lessons Learned

* Structured formats do not eliminate security risk.
* Client-side parsing must be treated as a security-sensitive operation.
* Trust assumptions should be minimized throughout application workflows.

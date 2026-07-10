# Lab: DOM-Based Cookie Manipulation

## Overview

This lab explores how client-side code that relies on cookie values can become vulnerable when security-sensitive decisions depend on user-controlled data.

## Root Cause

The application trusts information stored within browser cookies and uses those values without adequate validation.

## Key Concepts

* Cookie security
* Client-side trust boundaries
* Browser storage
* Data integrity

## Impact

Potential consequences include:

* Application logic manipulation
* Unauthorized functionality access
* Exposure of sensitive information
* Increased attack surface

## Detection Summary

Security testing revealed that cookie-derived values influenced application behavior in a security-relevant manner.

## Remediation

* Avoid trusting client-controlled storage
* Validate security-sensitive values server-side
* Use signed or protected tokens where appropriate
* Minimize reliance on browser-controlled data

## Lessons Learned

* Browser storage should not be treated as trusted.
* Security decisions belong on the server whenever possible.
* Data integrity is a critical component of application security.

# Lab: Exploiting Cache Server Normalization for Web Cache Deception

## Overview

This lab focuses on normalization behavior performed by cache servers. Security issues may arise when caching systems interpret requests differently from backend applications.

## Root Cause

The caching layer modifies or normalizes requests in a manner that differs from the origin application's interpretation, resulting in inconsistent security decisions.

## Key Concepts

* Cache server normalization
* Web Cache Deception
* Request processing
* Infrastructure security

## Impact

Potential consequences include:

* Information disclosure
* Exposure of authenticated content
* Unintended caching of dynamic responses
* Increased risk of privacy violations

## Detection Summary

Testing identified inconsistencies between cache server request processing and backend application behavior.

## Remediation

* Align normalization behavior across systems
* Review caching rules regularly
* Restrict caching of personalized content
* Implement strong cache-control directives

## Lessons Learned

* Caching infrastructure can influence application security.
* Request normalization should be reviewed from a security perspective.
* Infrastructure inconsistencies are a common source of complex vulnerabilities.

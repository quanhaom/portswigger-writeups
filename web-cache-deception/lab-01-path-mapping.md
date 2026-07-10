# Lab: Exploiting Path Mapping for Web Cache Deception

## Overview

This lab demonstrates how inconsistencies between URL routing logic and caching behavior can result in sensitive content being stored within a cache. Web Cache Deception occurs when content intended for authenticated users is mistakenly treated as cacheable static content.

## Root Cause

The application and caching infrastructure interpret URL paths differently. As a result, dynamic content may be processed by the application while simultaneously being considered cacheable by intermediary systems.

## Key Concepts

* Web Cache Deception
* URL path mapping
* Cache behavior
* Dynamic content exposure

## Impact

Potential consequences include:

* Disclosure of sensitive user information
* Exposure of authenticated content
* Privacy violations
* Unauthorized access to cached resources

## Detection Summary

Assessment activities revealed inconsistencies between application routing behavior and cache classification rules.

## Remediation

* Configure cache rules carefully
* Avoid caching authenticated content
* Apply Cache-Control headers appropriately
* Review routing and caching logic together

## Lessons Learned

* Security boundaries often extend beyond application code.
* Cache behavior must be evaluated alongside routing behavior.
* Misaligned infrastructure components can introduce significant risk.

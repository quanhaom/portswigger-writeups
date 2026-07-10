# Lab: Exploiting Origin Server Normalization for Web Cache Deception

## Overview

This lab demonstrates how normalization performed by origin servers can interact with caching behavior in unexpected ways. Differences in request handling may cause sensitive content to become cacheable.

## Root Cause

The origin server normalizes incoming requests before processing them, while caching systems evaluate requests using different logic. This discrepancy creates opportunities for cache deception scenarios.

## Key Concepts

* Request normalization
* Origin server behavior
* Cache security
* Infrastructure inconsistencies

## Impact

Potential consequences include:

* Exposure of user-specific content
* Unauthorized access to cached information
* Increased risk of information disclosure
* Security control bypass

## Detection Summary

Assessment activities revealed differences between how requests were normalized by the origin server and how they were classified by caching components.

## Remediation

* Standardize request normalization processes
* Restrict caching of authenticated responses
* Review infrastructure interactions
* Apply strict cache-control policies

## Lessons Learned

* Request normalization can have security implications.
* Application and infrastructure components must be evaluated together.
* Consistent request handling improves security.

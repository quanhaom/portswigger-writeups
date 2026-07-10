# Lab: Finding and Exploiting an Unused API Endpoint

## Overview

This lab highlights the security risks associated with legacy, deprecated, or undocumented API functionality. Endpoints that are no longer used by the application may still remain accessible.

## Root Cause

The application exposes functionality that remains available despite no longer being actively used by the user interface or primary application workflow.

## Key Concepts

* API Discovery
* Attack Surface Management
* Legacy Functionality
* Endpoint Enumeration

## Impact

Potential consequences include:

* Exposure of unintended functionality
* Access to outdated business logic
* Security control inconsistencies
* Increased attack surface

## Detection Summary

Security testing identified API endpoints that were not actively referenced by the application but remained accessible.

## Remediation

* Remove unused endpoints
* Maintain API inventories
* Conduct regular attack surface reviews
* Disable deprecated functionality

## Lessons Learned

* Unused functionality can still create security risk.
* Asset management is a key component of application security.
* Attackers often target forgotten or legacy features.

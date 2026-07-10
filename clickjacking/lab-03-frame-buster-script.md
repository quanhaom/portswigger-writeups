# Lab: Clickjacking with a Frame Buster Script

## Overview

This lab explores the limitations of client-side frame busting mechanisms. While frame buster scripts may provide some protection, they should not be considered a complete defense against clickjacking attacks.

## Root Cause

The application relies primarily on client-side controls rather than browser-enforced framing restrictions. This creates opportunities for attackers to bypass intended protections.

## Key Concepts

* Clickjacking
* Frame busting
* Client-side security controls
* Browser security mechanisms

## Impact

Potential consequences include:

* Unauthorized user actions
* Circumvention of security controls
* Exposure of sensitive functionality
* Increased attack reliability

## Detection Summary

Assessment activities revealed that framing protections depended on client-side behavior rather than robust browser security policies.

## Remediation

* Use X-Frame-Options
* Implement CSP frame-ancestors
* Avoid relying solely on JavaScript-based defenses
* Apply layered security controls

## Lessons Learned

* Client-side defenses can often be bypassed.
* Browser-enforced security controls provide stronger protection.
* Defense-in-depth is essential for UI security.

# Lab: Basic Clickjacking with CSRF Token Protection

## Overview

This lab demonstrates that the presence of CSRF protection alone does not necessarily prevent user interface redressing attacks. Clickjacking targets user interactions rather than directly attacking server-side request validation mechanisms.

## Root Cause

The application allows sensitive functionality to be embedded within a frame controlled by another website. As a result, users may unknowingly interact with hidden application elements.

## Key Concepts

* Clickjacking
* UI Redressing
* Frame-based attacks
* User interaction manipulation

## Impact

Potential consequences include:

* Unauthorized account actions
* Unintended user interactions
* Account configuration changes
* Abuse of legitimate user sessions

## Detection Summary

Assessment activities revealed that sensitive application functionality could be rendered inside an external frame without adequate restrictions.

## Remediation

* Implement X-Frame-Options
* Use Content-Security-Policy frame-ancestors
* Restrict framing of sensitive pages
* Apply defense-in-depth controls

## Lessons Learned

* CSRF protection does not eliminate clickjacking risk.
* User interface security is an important security boundary.
* Framing restrictions should be applied to sensitive functionality.

# Lab: Multistep Clickjacking

## Overview

This lab demonstrates how clickjacking attacks can target workflows that require multiple user interactions. Complex application processes may still be vulnerable when framing protections are absent.

## Root Cause

Sensitive multi-step functionality can be embedded within attacker-controlled interfaces, allowing user actions to be manipulated across multiple stages of a workflow.

## Key Concepts

* Clickjacking
* Multi-step workflows
* User interaction manipulation
* UI security

## Impact

Potential consequences include:

* Unauthorized account modifications
* Abuse of legitimate user sessions
* Increased attack success rates
* Compromise of sensitive workflows

## Detection Summary

Assessment activities showed that multiple stages of a security-sensitive workflow could be influenced through framed application content.

## Remediation

* Implement X-Frame-Options
* Use CSP frame-ancestors
* Introduce additional verification for sensitive actions
* Review security-critical user workflows

## Lessons Learned

* Multi-step processes are not inherently resistant to clickjacking.
* User interface security must be considered throughout an entire workflow.
* Browser-enforced framing controls provide the strongest protection.
